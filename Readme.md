
The **/etc/** folder contains individually exported the points from ETC (not all of them currently).

The **/y/** and **/z/** refer to an extended database of triangle centers - i.e. centers which are not in ETC currently. The main reason for having those is that it is easier to just calculate the coordinates of a potentially interesting triangle center and let it be used for property searching, instead of checking the properties of each point. Many of the unlisted points (surely many thousands!) are not interesting as triangle centers.

To identify a point refer to the *NonETCNames.csv* file and the following convention. Tradtitional ETC points are refered with X(n).
The following transformations have been used for descriptions of non-ETC points:

IsogConj - isogonal conjugate
IsotConj - isotomic conjugate
PolarConj - polar conjugate

CM1 - first X-circumconcevian conjugate introduced here: https://groups.io/g/euclid/message/5569 

    u/((v/a2 + w/a3)(v/b2 + w/b3) - u^2/(a1*b1)) 

CM2 - second X-circumconcevian image introduced here: https://groups.io/g/euclid/message/5576 

    u/((v/a2 - w/a3)(v/b2 - w/b3) - u^2/(a1*b1))

CM3 - third X-circumconcevian image introduced here: https://groups.io/g/euclid/message/5576 

    u/((v/a2 + w/a3)(v/b2 + w/b3) + u^2/(a1*b1))


**To submit a change make a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork) !** 
It may not be trivial if this is your first time working with Git version control.

If you want to submit a point for inclusion in ETC, you should either: manually remove the properties related to Y- and Z- points, or recalculate the properties, or submit a request and I will recalculate and prepare an ETC entry.