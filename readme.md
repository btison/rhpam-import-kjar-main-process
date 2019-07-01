#### Subprocesses with common main process

A RHPAM process illustrating how a common master process can be combined with multiple versions or flavours of a subprocess. This is based on the possibility to import a kjar into another kjar. The assets of the imported kjar become available in the main kjar.

* This project contains the main process, `main-process`.
* The `main-process` process definition has a _reusable sub-process node_.
* The _Called Element_ property of the subprocess node is set to the value `sub-process`.
* The `kmodule.xml` descriptor in `src/main/resources/META-INF` contains the definition of a named _kbase_ and _ksession_. Default unnamed kbase and ksession definitions cannot be used when importing a kjar into another kjar.
* The main process kjar will be imported into the subprocess kjar. As such it does not need to be deployed on its own.