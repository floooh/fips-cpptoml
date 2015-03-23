# fips-cpptoml

- cpptoml: https://github.com/skystrife/cpptoml
- fips: https://github.com/floooh/fips/

Requires C++ exceptions enabled, add the following line
to you toplevel CMakeLists.txt file before fips_setup()
is called, or build with a fips config that sets FIPS\_EXCEPTIONS to ON:

```cmake
set(FIPS_EXCEPTIONS ON CACHE BOOL "Enable C++ exceptions" FORCE)
fips_setup()
...
```

This is a header-only lib, simply add to your fips.yml as import
and include cpptoml.h:

```yaml
imports:
    fips-cpptoml:
        git:    https://github.com/floooh/fips-cpptoml
```

```cpp
#include "cpptoml.h"
```

