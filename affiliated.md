Becoming an Affiliated Package
------------------------------

If you are a developer of an analysis package and would like your
package to become affiliated with the sckit-xray project, leave a
message on the (???) group requesting affiliated package status. If
you are comfortable doing so, you should also create a pull request
adding your package to the registry file on the (???).  The Astropy
coordination commitee and community will then consider your package
based on the standards below.

-   It should use [classes and functions from the scikit-xray
    package](http://github.com/scikit-xray/scikit-xray) wherever possible and
    appropriate. This facilitates re-use of code and sharing of
    resources.
-   The package should have documentation that adequately explains the
    use of the package, at standards comparable to scikit-xray.
    Additionally, user-facing classes and functions should all have
    docstrings. We suggest using sphinx, with the numpydoc-like
    docstring standards used by
    scikit-xray.
    but this is not a strict requirement as long as the documentation is
    of comparable quality.
-   The package should make a best-effort to include an easy-to-run test
    suite that covers its intended functionality. We realize this is not
    always possible, but when it is, a test suite is a crucial element
    of stable software and reproducible science.
-   The package developer(s) should make an effort to connect with the
    sckit-xray developer community, including developers from the core
    scikit-xray package or any related affiliated packages.
-   While not a strict requirement, we also provide coding
    guidelines
    that will make your code easier to read by members of the community.
-   We strongly encourage affiliated packages be compatible with Python
    2.7. Tips for how to acheive this are given in the revelant section
    of the coding
    guidelines.
    The recommended route is to use [six](http://pythonhosted.org/six/).

If your package is judged by the coordination committe to meet these
standards, it will be added to the affiliated package registry. If the
package is not quite at these standards, but working towards them, the
package will be given "provisional" status. Provisional packages will
be re-evaluated yearly by the coordinating committee, or earlier if
the package author requests a review. (You can e-mail a member of the
coordination committee to request such a review). In this
re-evaluation, the committee will look at progress the package has
made over the previous year. If it has been advanced sufficiently to
meet the standards above, it will be considered a full affiliated
package (no longer provisional). If it has made some progress but is
not yet up to the standards, provisional status will be renewed for a
year. If no progress seems to be being made, the committee will
contact the authors and determine what their plans are to improve the
situation. Based on that, the committee may decide to renew the
provisional status, or remove the package from the registry.

Affiliated Package Template
---------------------------

If you are considering creating a new astronomy package and would like
it to be an Astropy affiliated package, we provide a package template
to make it much easier to meet these standards. It provides the
necessary structure to generate documentation like that used in the
astropy package, a ready-to-use testing framework, and a variety of
tools that streamline tasks like user configuration, caching
downloaded files, or linking C-compiled extensions. More details on
this template are available in the usage instructions for the
template.
