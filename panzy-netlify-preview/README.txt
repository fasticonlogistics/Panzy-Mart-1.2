PANZY STATIC PREVIEW - NETLIFY DEPLOYMENT
========================================

This folder is the free, static storefront preview. It runs independently of
the separate WordPress + WooCommerce installation.

DEPLOY THIS FOLDER FROM GITHUB
------------------------------
Keep the repository-root netlify.toml and the entire "panzy-netlify-preview"
folder in the repository. Do not upload only the HTML files: the
"panzy-preview-assets" subfolder contains the logo and all product, category,
and hero images and is required for images to show.

In Netlify, open the panzy-mart-12 site's:
Project configuration > Build & deploy > Continuous deployment > Build settings

The repository-root netlify.toml sets Base directory to the repository root
and Publish directory to panzy-netlify-preview. No build command is needed.

Leave the Build command empty. The root configuration is used automatically
for Git-connected deploys. Trigger "Deploy site" from the Deploys page after
the changes reach the main branch.

The deployed site should contain index.html at its root. If Netlify shows a
404, check the exact base directory, the branch selected for deploy, and that
the latest commit contains this folder and netlify.toml.

After deployment, these image URLs should open successfully (HTTP 200):
/panzy-preview-assets/panzy-logo.png
/panzy-preview-assets/hero-living.jpg

ALTERNATIVE: UPLOAD THIS FOLDER'S CONTENTS TO A NEW REPOSITORY ROOT
-----------------------------------------------------------------
If you create a separate GitHub repository just for the preview, upload the
contents of this folder (not an additional enclosing folder) to the repository
root, including this folder's netlify.toml, which publishes ".". Do not copy
the parent repository's netlify.toml into that standalone repository. Connect
that repository in Netlify and leave Base directory empty.

PAGES
-----
Home:          /
Shop:          /shop.html
Categories:    /categories.html
About:         /about.html
Contact:       /contact.html

LIMITATIONS
-----------
This is a static demonstration. Its sample storefront/cart interactions are
not a live WooCommerce store and do not accept real orders or payments. For a
managed catalogue, checkout, and orders, install panzy-theme.zip on WordPress
with WooCommerce and configure the store there.
