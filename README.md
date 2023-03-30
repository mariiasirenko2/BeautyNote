# BeautyNote

## Endpoints by domain object

### Me (client or master abstraction)

<pre>
GET  /me # Get profile info
GET  /me/clients # Get clients list (for master only)
GET  /me/services?status=... # Get attached services (all or by status)
PUT   /me # Edit profile (all fields) 
PATCH /me # Edit profile (certain fields)
</pre>

### Client

<pre>
GET  /clients/{client-id} # Get information about certain client
GET /clients/{client-id}/conversation # Get converstation id for certain client / Start a conversation with certain client (master only)
</pre>

### Master

<pre>
GET  /masters # Get list of masters
GET  /masters/{master-id} # Get information about certain master
GET /masters/{master-id}/conversation # Get conversation id with certain master / Start a conversation with certain client (client only)
GET  /masters/{master-id}/services # Get certain master services
</pre>

### Service

<pre>
GET  /services # Get all services available
POST /services # Add new service (master only)

GET  /services/{service-id} # Get information about certain service
PUT   /services/{service-id} # Edit certain service (all fields)
PATCH /services/{service-id} # Edit certain service (certain fields)

GET  /services/{service-id}/reviews # Get reviews for certain service

GET /services/{service-id}/reviews/{review-id}/comments # Get comments for certain review
POST /services/{service-id}/reviews/{review-id}/comments # Add comment for certain review
PUT   /services/{service-id}/reviews/{review-id}/comments/{comment-id} # Edit comment for certain review
</pre>

### Slot

<pre>
GET /masters/{master-id}/slots # Get slots for certain master
GET /service/{service-id}/slots # Get slots for certain service
</pre>

#### Client side
<pre>
POST /slots/{slot-id}/reviews # Add review to sertain slot (service beneath it)
PUT /slots/{slot-id}/reviews/{review-id} # Edit review (+edit time politic)
</pre>

### Conversation

<pre>
GET  /conversations # Get the list of available conversations
? GET  /conversations/{conversation-id} # Get the information about certain conversation

GET  /conversations/{conversation-id}/messages # Get messages for certain conversation
POST /conversations/{conversation-id}/messages # Add message for certain conversation

PUT  /conversations/{conversation-id}/messages/{message-id} # Edit certain message
DEL  /conversations/{conversation-id}/messages/{message-id} # Delete certain message
</pre>

### Images
<pre>
GET /images/{image-id} # Get image by id
POST /images # Add image
</pre>

### ??? Voice ???
<pre>
</pre>
