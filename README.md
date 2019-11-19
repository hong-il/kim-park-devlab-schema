## Kim&Park Devlab

A schema for a developers' blog

### Table : posts

* **post_id** : (Long), Primary key and auto increments for ID

* **title** : (String), Title of post

* **subtitle** : (String), Subtitle of post

* **content** : (Text), Content of post

* **createdBy** : (Long), ID of the user who created this post

* **lastModifiedBy** : (Long), ID of the user who modified this post

* **createdDate** : (LocalDateTime), When post first created

* **lastModifiedDate** : (LocalDateTime), Last time when post modified

### Table : posts_images

* **post_id** : (Long)

* **image_id** : (List)

### Table : images

* **image_id** : (Long), Primary key and auto increments for ID

* **image_path** : (String), Path to image on server

* **image_size** : (Integer), Image size on server

* **createdBy** : (Long), ID of the user who created this photo

* **lastModifiedBy** : (Long), ID of the user who modified this photo

* **createdDate** : (LocalDateTime), When image first uploaded

* **lastModifiedDate** : (LocalDateTime), Last time when image modified

### Table : posts_comments

* **post_id** : (Long) 

* **comment_id** : (List)

### Table : comments

* **comment_id** : (Long), Primary key and auto increments for ID

* **comment_master_id** : (Long), When dependent on comments, the ID of the master comment

* **comment** : (Text), A simple text field containing the comment

* **createdBy** : (Long), ID of the user who created this comment

* **lastModifiedBy** : (Long), ID of the user who modified this comment

* **createdDate** : (LocalDateTime), When comment first created

* **lastModifiedDate** : (LocalDateTime), Last time when comment modified

### Table : posts_tags

* **post_id** : (Long) 

* **tag_id** : (List)

### Table : tags

* **tag_id** : (Long), Primary key and auto increments for ID

* **tag** : (Text), A simple text field containing the tag

### Table : likes

* **post_id** : (Long)

* **like** : (boolean), True when like first clicked, false when clicked one more (loop)

* **createdBy** : (Long), ID of the user who liked the post

* **lastModifiedBy** : (Long), ID of the user who liked(cancle) this post

* **createdDate** : (LocalDateTime), When this like first clicked

* **lastModifiedDate** : (LocalDateTime), Last time when like(cancle) clicked

### Table : users

* **user_id** : (Long), Primary key and auto increments for ID

* **username** : (String), Username(Unique index)

* **email** : (String), Email address(Unique index)

* **password** : (String), Securing password digests

* **first_name** : (String), First name of user

* **last_name** : (String), Last name of user

* **last_ip** : (String), Last known user IP address

* **createdBy** : (Long), ID of the user who signed up

* **lastModifiedBy** : (Long), ID of the user who modified user data 

* **createdDate** : (LocalDateTime), When this user signed up

* **lastModifiedDate** : (LocalDateTime), Last time when this user signed in
