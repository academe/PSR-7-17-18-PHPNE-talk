## PSR-7 Interfaces

* Psr\Http\Message\MessageInterface
  * Psr\Http\Message\RequestInterface
    * Psr\Http\Message\ServerRequestInterface
* Psr\Http\Message\ResponseInterface

* Psr\Http\Message\StreamInterface
* Psr\Http\Message\UriInterface
* Psr\Http\Message\UploadedFileInterface

---

## PSR-17 Factories

* A factory interface for each PSR-7 interface <!-- .element: class="fragment" -->
* A client needs a ResponseInterface factory <!-- .element: class="fragment" -->
* A package may need any of the factories <!-- .element: class="fragment" -->
* An implementation may have a separate class for each factory... <!-- .element: class="fragment" -->
* or may combine them into one factory <!-- .element: class="fragment" -->

---

## PSR-17 Factory Interfaces

* Psr\Http\Message\RequestFactoryInterface
* Psr\Http\Message\ServerRequestFactoryInterface
* Psr\Http\Message\ResponseFactoryInterface

* Psr\Http\Message\StreamFactoryInterface
* Psr\Http\Message\UriFactoryInterface
* Psr\Http\Message\UploadedFileFactoryInterface

---

## PSR-17 Implementations

https://packagist.org/providers/psr/http-factory-implementation <!-- .element: style="background-color: black" -->

![](slides/images/http-factory-implementations.png)

Notes:

* No idea where you find a list of "providers"
* Or what to put into the "provide" element of your composer.json
* These are virtual packages
