## PSR-18: HTTP Client

* https://www.php-fig.org/psr/psr-18/
* Interface for a client
* Very simple - just one method and some exceptions
* HTTP errors do not throw exceptions

Notes:

* Jump straight to the client.
* It is the client that knows how to serialise and send a request.
* The client knows how to receive, deserialise and deliver the response.
* Exceptions only thrown when the application can not parse the response, e.g a timeout.

---

## The Old Way

* A package needs to send requests
* It requires a specific client (a dependency):
  * Guzzle <!-- .element: class="fragment" -->
  * Zend Diactoros <!-- .element: class="fragment" -->
  * Curl, Yii2 Httpclient, Buzz, Requests, Httpful, Unirest PHP, ... <!-- .element: class="fragment" -->

Notes:

* A coder would in the past have to choose a client.
* Constructing a request would be done through the client in the way the client specifies.
* Lots of clients, and they can clash with other dependencies.

---

## The PSR-18 Way

* A package needs to send requests
* It is provided with a PSR-18 client to use (DI)
* The client is implementation agnostic

Notes:

* DI - Dependency Inversion.
* Any PSR-18 client will work.

---

## The PSR-18 Interface

The client will send a request and return a response.

```php
namespace Psr\Http\Client;

use Psr\Http\Message\RequestInterface;
use Psr\Http\Message\ResponseInterface;

interface ClientInterface
{
    public function sendRequest(RequestInterface $request):
        ResponseInterface;
}
```

Notes:

* Asynchronous is not a part of this spec.
* HTTPlug, a predecessor of PSR-18 does have an async client.
* Just a quick overview of PSR-7 follows.
