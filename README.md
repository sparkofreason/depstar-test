# depstar-test

On Windows, `clojure -A:uberjar` fails with:

```
PS C:\Users\dave\Projects\uberjar-test> clojure -A:uberjar
{:warning "clashing jar item", :path "edu/emory/mathcs/utils/ConcurrencyUtils$CustomExceptionHandler.class", :strategy :noop}
{:warning "clashing jar item", :path "edu/emory/mathcs/utils/ConcurrencyUtils$CustomThreadFactory.class", :strategy :noop}
{:warning "clashing jar item", :path "edu/emory/mathcs/utils/ConcurrencyUtils.class", :strategy :noop}
Exception in thread "main" java.nio.file.NoSuchFileException: C:\Users\dave\AppData\Local\Temp\uberjar16821059387554463855\uncomplicate\neanderthal\aux.clj
        at java.base/sun.nio.fs.WindowsException.translateToIOException(WindowsException.java:85)
        at java.base/sun.nio.fs.WindowsException.rethrowAsIOException(WindowsException.java:103)
        at java.base/sun.nio.fs.WindowsException.rethrowAsIOException(WindowsException.java:108)
        at java.base/sun.nio.fs.WindowsFileSystemProvider.newByteChannel(WindowsFileSystemProvider.java:231)
        at java.base/java.nio.file.spi.FileSystemProvider.newOutputStream(FileSystemProvider.java:478)
        at java.base/java.nio.file.Files.newOutputStream(Files.java:219)
        at java.base/java.nio.file.Files.copy(Files.java:3066)
        at hf.depstar.uberjar$copy_BANG_.invokeStatic(uberjar.clj:92)
        at hf.depstar.uberjar$copy_BANG_.doInvoke(uberjar.clj:85)
        at clojure.lang.RestFn.invoke(RestFn.java:467)
        at hf.depstar.uberjar$eval190$fn__191$fn__192.invoke(uberjar.clj:141)
        at hf.depstar.uberjar$consume_jar.invokeStatic(uberjar.clj:106)
        at hf.depstar.uberjar$consume_jar.invoke(uberjar.clj:98)
        at hf.depstar.uberjar$eval190$fn__191.invoke(uberjar.clj:133)
        at clojure.lang.MultiFn.invoke(MultiFn.java:239)
        at hf.depstar.uberjar$copy_source.invokeStatic(uberjar.clj:174)
        at hf.depstar.uberjar$copy_source.invoke(uberjar.clj:172)
        at hf.depstar.uberjar$run$fn__224$fn__225.invoke(uberjar.clj:229)
        at clojure.core$run_BANG_$fn__8775.invoke(core.clj:7715)
        at clojure.lang.PersistentVector.reduce(PersistentVector.java:343)
        at clojure.core$reduce.invokeStatic(core.clj:6827)
        at clojure.core$run_BANG_.invokeStatic(core.clj:7710)
        at clojure.core$run_BANG_.invoke(core.clj:7710)
        at hf.depstar.uberjar$run$fn__224.invoke(uberjar.clj:229)
        at hf.depstar.uberjar$run.invokeStatic(uberjar.clj:228)
        at hf.depstar.uberjar$run.invoke(uberjar.clj:224)
        at hf.depstar.uberjar$_main.invokeStatic(uberjar.clj:235)
        at hf.depstar.uberjar$_main.invoke(uberjar.clj:233)
        at clojure.lang.AFn.applyToHelper(AFn.java:154)
        at clojure.lang.AFn.applyTo(AFn.java:144)
        at clojure.lang.Var.applyTo(Var.java:705)
        at clojure.core$apply.invokeStatic(core.clj:665)
        at clojure.main$main_opt.invokeStatic(main.clj:491)
        at clojure.main$main_opt.invoke(main.clj:487)
        at clojure.main$main.invokeStatic(main.clj:598)
        at clojure.main$main.doInvoke(main.clj:561)
        at clojure.lang.RestFn.applyTo(RestFn.java:137)
        at clojure.lang.Var.applyTo(Var.java:705)
        at clojure.main.main(main.java:37)
```
