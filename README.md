[![GitLab CI Build
Status](https://gitlab.com/dickoa/cgal4h/badges/master/pipeline.svg)](https://gitlab.com/dickoa/cgal4h/pipelines)


# cgal4h

This package provides an R interface to the header-only C++ [CGAL](https://www.cgal.org) version 4 library

This package is using the latest release of the version 4 of  [CGAL](https://www.cgal.org).

## Install


Install the development version with the `remotes` R package

```r
remotes::install_gitlab("dickoa/cgal4h")
```

## Using cgal4h

In order to use `cgal4h` in your own R package, you need to add it to the `LinkingTo` field in the DESCRIPTION field of R
package. You also need to have the following C++ compiler flag.

```r
-DCGAL_HEADER_ONLY=1
```

If you are using `Rcpp` don't forget to add a dependency to `cgal4h` to your cpp files **before** a call to `#include <Rcpp.h>`

```r
// [[Rcpp::depends(cgal4h)]]

#include <Rcpp.h>
```

## Missing headers

Because of portability issues not all headers are included in this package, the following components are currently missing:

- `CGAL/Algebraic_kernel_for_circles`
- `CGAL/Algebraic_kernel_for_spheres`
- `Polygon_mesh_processing/internal`
- `CGAL/Shape_detection/`

## License

This package is provided under the [GPL-3](https://www.gnu.org/licenses/gpl-3.0.en.html).

The CGAL library uses the dual license [GPL-3](https://www.gnu.org/licenses/gpl-3.0.en.html). | [LGPL-3](https://www.gnu.org/licenses/lgpl-3.0.en.html). More information can be found at [https://www.cgal.org/license.html](https://www.cgal.org/license.html).
