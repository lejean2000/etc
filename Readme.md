

The **/etc/** folder contains individually exported the points from ETC (not all of them currently).

The **/y/** and **/z/** refer to an extended database of triangle centers - i.e. centers which are not in ETC currently. The main reason for having those is that it is easier to just calculate the coordinates of a potentially interesting triangle center and let it be used for property searching, instead of checking the properties of each point. Many of the unlisted points (surely many thousands!) are not interesting as triangle centers.

To identify a point refer to the *NonETCNames.csv* file and the following convention. Tradtitional ETC points are refered with X(n). The rest follow these https://github.com/lejean2000/etc/wiki/Naming-Conventions.


**To submit a change make a [pull request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork) !** 
It may not be trivial if this is your first time working with Git version control.

If you want to submit a point for inclusion in ETC, you should either: manually remove the properties related to Y- and Z- points, or recalculate the properties, or submit a request and I will recalculate and prepare an ETC entry.

If you choose to remove the Y- and Z- properties yourself, here is an easy procedure which will remove most (not all!) Y and Z properties.

If you use Wolfram Mathematica you can just pass the whole text entry to the following function:

    reg = "[, ]*{([Y|Z]*?[\\d, \\(\\)ABCX])*[Y|Z].*?\}"
    StringReplace[somestring, RegularExpression[reg] -> ""]

Alternatively :

1. Navigate to https://regex101.com
2. In the left panel above choose Python, and in the left panel below choose Substitution.
3. Paste the following regex in the "Regular expression" field on top:

       \[, ]*{([Y|Z]*?[\d, \(\)ABCX])*[Y|Z].*?\}

4. Paste the ETC entry in the textbox. Make sure you have a new line at the end.
5. In the textbox below will be your entry, stripped of Y and Z properties.

