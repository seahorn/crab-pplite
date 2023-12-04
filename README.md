# Native interface between Crab and PPLite #

This repository allows calling all the [PPLite](https://www.cs.unipr.it/~zaffanella/PPLite) domains from the [Crab](https://github.com/seahorn/crab)
library by using a native interface instead of the Apron interface.  The benefit is speed: using the native interface is much faster than the Apron interface.
The header file [pplite_native_wrapper](https://github.com/seahorn/crab-pplite/blob/main/pplite_native_wrapper.hpp) defines a Crab abstract domain, called `pplite_domain`, that implements
all the abstract operations by calling their counterpart PPLite
operations.

For any question or issue, please email Matteo Boroni Grazioli
(matteboro@unipr.it), who is the main developer of this interface, and
Enea Zaffanella (enea.zaffanella@unipr.it).

## How to use it ##

When you compile the Crab library (see instructions [here](https://github.com/seahorn/crab#compilation-and-installation)), add the `cmake` option `-DCRAB_USE_PPLITE_NATIVE=ON`.
This option will download automatically this repo and copy it in the Crab `domains` directory.
