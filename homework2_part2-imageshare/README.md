

---

shareimage
========

A simple client-side photo sharing site.
-----------------
The security model of this simple photo sharing app is predicated on having
locations being unguessable. We construct paths into Firebase using a hash of
the file being uploaded. Then, anyone that has access to the share-able link
can then lookup the location in Firebase and view its contents.

A simple rule set is required to make sure none of the keys are enumerable
from Firebase. This prevents retrieval of the keys from any of the Firebase
clients, including REST endpoints. We also add a write rule to the photos so
that once the data has been written, no one can override or delete data that
already exists. 

License
-------
[MIT](http://firebase.mit-license.org), except share.js.


