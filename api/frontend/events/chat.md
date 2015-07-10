# Chat Event

Chat events are fired when a user sends a chat message. This is also sent by the system for maintenance messages and
moderation messages. "/me" or "/em" causes an "emote" event to be fired instead of a "message" event.

### Packet Example

And an example of the full event package looks like:

```js
{
    cid: "4175640-1436477722736", //Chat ID
    message: "I&#39;m here", //Message
    sub: 0, //Is Subscriber Boolean
    timestamp: "10:35pm", //Timestamp
    type: "message", //Message Type
    uid: 4175640, //Sender ID
    un: "Mayniac" //Sender Username
}
```

Where type can be a string equalling "message", "emote", "moderation", "system".

Where message is the content of the message as seen on plug, un is the username of the sender, and uid is the id of
the sender.

The sub value is a boolean of whether the user is a subscriber or not.

The cid value is the chat ID, this is not a unique value as messages stack, it is comprised of the sender ID split with 
a dash, and followed by the message number.

### Code Example

```js

API.on(API.CHAT, function(data){
    //This will log the packet of the chat event
    console.log(data);
});

```
