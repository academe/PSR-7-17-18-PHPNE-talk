## Summary

* These PSRs have been adopted widely by client and message libraries <!-- .element: class="fragment" -->
* Not adopted much by users of clients and message libraries <!-- .element: class="fragment" -->
* Relatively simply to upgrade <!-- .element: class="fragment" -->
* Lots more detail not covered in this short talk <!-- .element: class="fragment" -->

Notes:

* Users include payment gateways, API libraries, swagger/OpenAPI code generation etc.
* Omnipay is switching over

---

## The Interfaces

* PSR-7 request and responses
* PSR-17 factories to create PSR-7 messages
* PSR-18 a client to send and receive requests

---

## Implementations

On packagist.org look for:

* PSR-7: providers/psr/http-message-implementation
* PSR-17: providers/psr/http-factory-implementation
* PSR-18: providers/psr/http-client-implementation

---

## Using These PSRs

* For your frameworks and your packages <!-- .element: class="fragment" -->
* Instantiate client and factories in framework... <!-- .element: class="fragment" -->
* ...inject them into your libraries. <!-- .element: class="fragment" -->
* Discovery: do you need it? <!-- .element: class="fragment" -->
* Pick your favourite implementations or use what's provided. <!-- .element: class="fragment" -->

Notes:

* The framework may dictate which client and factories are used.
* Another package my dictate this.

---

## Thank You

* Jason Judge
* @JasonDJudge
* jason@consil.co.uk
* https://github.com/academe/PSR-7-17-18-PHPNE-talk
