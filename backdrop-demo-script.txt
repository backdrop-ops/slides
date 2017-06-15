Backdrop CMS Demo
=================

Preparation
-----------

- Install Devel Generate and create 100 nodes and comments.
- Uninstall Devel Generate when done!
- Create site on Pantheon by clicking button on BackdropCMS.org


Feature hit-list
----------------

Rich Text Editor (CKEditor):

- Enabled out-of-box.
- Custom plugins for inserting images and links.

Fields:
- Date, Link, Email

Installer:

- Enable themes and modules through the UI (do on Pantheon, switch to SFTP mode first)


Introduction
------------

- Show out of box responsiveness.

- Demonstrate admin menu
  - Responsiveness by resizing window.
  - Search capability
    - Search for "Views", use tab key to switch to list of links.
    - Go to Views admin page.

Views
-----

- Views: Add new view
  - "Top posts" view of Posts

Layouts
-------

- Access Layout admin through search or Structure > Layouts.

- Add new layout for "frontpage"
  - Use 3/3/4 layout
  - Add "Top posts" view to the center area
- Add new layout for Posts (machine name node_post)
  - Use 2-column layout
  - Specify node/% as path (note the auto-complete contexts, demonstrate changing to user/% and back to node/%)
  - Add conditional for Node: Type, specify matching posts only.
  - Add "Top posts" view to the left sidebar
- Optional: Add new layout for Pages (machine name node_page)
  - Use 1-column layout
  - Specify node/% as path
  - Add conditional for Node: Type, specify matching pages only.
  - Save with no other changes.
- Visit a node post, show sidebar blocks.
- Visit a node page. Show different layout.

Configuration management
------------------------

- Open the filesystem of the site. Visit files/config_[hash]/active
- Show the configuration file for the create layout (layout.layout.node_article.json)
- Note that you could manage these configuration files in Git, but we're going to use the UI.
- Access Configuration Management through search or Configuration > Development > Configuration Management
- Export entire site as archive
- Import entire site into Pantheon (test this first!)
  - Note that enabled module list must be the same between environments.
  - Config management will not allow you to delete content types or fields through import (unless those fields/types are empty).
