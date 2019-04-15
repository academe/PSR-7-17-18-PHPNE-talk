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

* There is a factory interface for each PSR-7 message
* A client will need a `ResponseInterface` factory
* A package may need any number of the other factories
* An implementation may provide a separate class for each factory...
* or may combine them into one factory implementing all the inerfaces
