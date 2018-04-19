# PHP
php is an interpreted language

* Get
  * Changes the URL
  * Not great for file uploads
  * Those requests are logged on the servers
  * URL can be copy pasted

* Post
  * URL doesn't change
  * No limit on the character length
  * Good for sensitive data


> When the user submits a form using post, send a get request with a 301 or a 302 request so that the back button takes the user between get paths not post.

## Documentation

http://us3.php.net/manual/en/

## Separating customers
Apache is good for securing the server but not to separate customers data from each other. Files are owned by apache. There are solutions that make each file owned by the customer.

Solutions
* SUPHP: Substitute user php **Deprecated**

> `chmod 644` makes the files world readable
