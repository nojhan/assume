Assume
======

- Assume is a smarter assert replacement (C++03).
- Assume is handy. LHS/RHS values are printed as long as they are `ostream` friendly.
- Assume is cross-platform. Crash handler fallbacks to `assert()` symbol.
- Assume is header only.
- Assume is zlib/libpng licensed.

## Sample

```c++
#include "assume.hpp"

int main() {
    int a = 1, b = 2;

    assume( a < b );
    assume( a > b );
}
```

## Showcase

```c++
#~/> g++ sample.cc && ./a.out
<assume.hpp> says: expression failed! (a > b) -> (1 > 2) -> (unexpected) at sample.cc:7
```

## Changelog

- v1.0.2 (2019-07-23)
  - fix a reorder warning
- v1.0.1 (2015/09/19)
  - Force flushed pipes
- v1.0.0 (2015/08/07)
  - Initial C++03 version
