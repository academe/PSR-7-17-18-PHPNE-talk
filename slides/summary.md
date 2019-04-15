## Summary

* These PSRs have been adopted widely
* Relatively simply to upgrade
* Enough details for an hour's talk

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

* Instantiate client and factories in framework...
* ...inject them into your libraries.
* Discovery: do you need it?
* Pick your favourite implementations or use what's provided.

Notes:

* The framework may dictate which client and factories are used.
* Another package my dictate this.

---

## Thank You

* Jason Judge
* @JasonDJudge
* jason@consil.co.uk
* https://github.com/academe/PSR-7-17-18-PHPNE-talk
