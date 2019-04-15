## PSR-18: HTTP Client

* https://www.php-fig.org/psr/psr-18/
* Interface for a client
* Very simple - just one method and some exceptions
* HTTP errors do not throw exceptions

---

## The Old Way

* A package needs to send requests
* It required a client (a dependency):
  * Guzzle <!-- .element: class="fragment" -->
  * Zend Diactoros <!-- .element: class="fragment" -->
  * Curl, Yii2 Httpclient, Buzz, Requests, Httpful, Unirest PHP, ... <!-- .element: class="fragment" -->

---

## The PSR-18 Way

* A package needs to send requests
* It is provided with a PSR-18 client to use (DI)
* The client is implementation agnostic

Notes:

* DI - Dependency Inversion

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
* Just a quick overview of PSR-7 follows.