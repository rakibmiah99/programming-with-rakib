```php
composer require pusher/pusher-php-server
```

.env pusher configuration 
```shell
PUSHER_APP_ID="your-pusher-app-id"
PUSHER_APP_KEY="your-pusher-key"
PUSHER_APP_SECRET="your-pusher-secret"
PUSHER_HOST=
PUSHER_PORT=443
PUSHER_SCHEME="https"
PUSHER_APP_CLUSTER="mt1"

```

Then, set the `BROADCAST_CONNECTION` environment variable to `pusher` in your

```shell
BROADCAST_CONNECTION=pusher
```


# Front End 

Include the [pusher-js](https://github.com/pusher/pusher-js) script tag on your page.
```html
<script src="https://js.pusher.com/8.0.1/pusher.min.js"></script>
```

**create pusher instance** 
```js
var pusher = new Pusher("APP_KEY", { 
	cluster: "APP_CLUSTER",
});

//Another Way to create 
var pusher = new Pusher({  
	appId: "APP_ID",
	key: "APP_KEY",
	secret: "APP_SECRET",
	cluster: "APP_CLUSTER",
});
```

**Subscribe to a channel**
```js
var channel = pusher.subscribe("my-channel");
```

**Listen for events on your channel**
```js
channel.bind("my-event", (data) => {
	// Method to be dispatched on trigger.
});
```

**Trigger events from your server**
```js
pusher.trigger("my-channel", "my-event", { 
	message: "hello world" 
});
```



# Server Configure

**If you want directly send by create pusher instance create** 

```php
$pusher = new Pusher(env('PUSHER_APP_KEY'), env('PUSHER_APP_SECRET'), env('PUSHER_APP_ID'), [  
    'cluster' => env('PUSHER_APP_CLUSTER'),  
    'host' => env('PUSHER_HOST') ?: 'api-'.env('PUSHER_APP_CLUSTER', 'mt1').'.pusher.com',  
    'port' => env('PUSHER_PORT', 443),  
    'scheme' => env('PUSHER_SCHEME', 'https'),  
    'encrypted' => true,  
    'useTLS' => env('PUSHER_SCHEME', 'https') === 'https',  
]);  

$response = $pusher->trigger('my-channel', 'my-event', 'data');
```


**By Laravel Event Broadcast** 

set  env `BROADCAST_CONNECTION`
```shell
BROADCAST_CONNECTION=pusher
```

create an event  and implements `ShouldBroadcastNow`

```php
class SendData implements ShouldBroadcastNow  
{  
    use InteractsWithBroadcasting;  
  
    public $message;  
    /**  
     * Create a new event instance.     */    public function __construct($message)  
    {  
        $this->message = $message;  
    }  
  
    /**  
     * Get the channels the event should broadcast on.     *     * @return array<int, \Illuminate\Broadcasting\Channel>  
     */    public function broadcastOn(): array  
    {  
        return [  
            new Channel('my-chanel'),  
        ];  
    }  
  
    public function broadcastAs(): string  
    {  
        return 'my-event';  
    }  
  
   //data pass from here 
    public function broadcastWith(): array{  
        return [  
            'message' => $this->message,  
        ];  
    }  
}
```

call event 
```php
event(new SendData('fjfj'));
```