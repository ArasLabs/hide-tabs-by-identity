# Hiding Relationship Tabs in an Item Window by Identity

It may be necessary that only certain users or groups are able to view the multiple relationships to a single item.

This document gives you an example for how to either remove the specific tabs completely or just disable them for users that do not belong the the property identity.

## History

This project and the following release notes have been migrated from the old Aras Projects page.

Release | Notes
--------|--------
[v1](https://github.com/ArasLabs/search-filtered-item-browser/releases/tag/v1) | Initial Release

#### Supported Aras Versions

Project | Aras
--------|------
[v1](https://github.com/ArasLabs/search-filtered-item-browser/releases/tag/v1) | 9.2.0 SP3

## Installation

#### Important!
**Always back up your code tree and database before applying an import package or code tree patch!**

### Install Steps

The following sample is used to remove the tabs for “Quality Planning Documents” and “Changes” on the form for the Part ItemType for all users except those that belong to the Quality Planning identity.   You are also able to disable the forms so they are visible to the user, but unable to be clicked on.  To achieve these results following these instructions:

1. Log into Aras Innovator as an Admin.
2. From the TOC select **Administration > Methods** and create a new Client Side Java Script Method. Name it as you please.
3. Insert the code from the end of [the document](./Documentation/Aras%20Innovator-%20How%20to%20Remove%20or%20Disable%20Rel%20Grid%20Tabs.doc). (Note: The code currently removes the tab, the code to disable the tab is commented out)
4. Save, Unlock, and Close the method.
5. From the TOC select **Administration > Form** and edit the form of the ItemType you want to apply the method to (For the sample code written we use the Part Form).
6. Select the “Form Event” tab and add a new Relationship.
7. Select your newly created method and attach the “onLoad” event to it
8. Save, Unlock, and Close the form.

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request

## Credits

Created by Aras Corporation Support.

## License

Published to Github under the MIT license. See the [LICENSE file](./LICENSE.md) for license rights and limitations.
