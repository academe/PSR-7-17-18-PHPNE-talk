## Discovery

* Instead of DI, a library can discover a suitable implementation installed <!-- .element: class="fragment" -->
* However, it needs to know the discovery service is installed <!-- .element: class="fragment" -->
* Maybe good for late instantiation <!-- .element: class="fragment" -->
* Probably more a convenience for legacy libraries <!-- .element: class="fragment" -->
* It gets complicated fast <!-- .element: class="fragment" -->

Notes:

* Omnipay is moving to discovery, but only because people expect it.
* Late instantiation: create the factories only when/if needed
