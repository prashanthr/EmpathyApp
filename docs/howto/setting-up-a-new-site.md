DocVer: 0.1


### Creating a new subdomain

Prerequisites: Access to cPanel (at arvixe) needed

1. Login in with cPanel

2. Under the heading "domains" you can find "subdomains"

3. Create a new subdomain, please choose the name of a person known for his/her empathy (examples: mandela, kuanyin)



### Wordpress installation

Prerequisites: Access to cPanel (at arvixe) needed

1. Login in with cPanel

2. search for "softaculous" and click this icon

3. find wordpress and click "install"

4. wordpress install settings:
  * use the subdomain created earlier
  * use a descriptive name for the db (preferrable the same name as the subdomain, but only 7 characters are allowed)
  * "in directory": remove "wp" from the path so this field is empty *(this is important!)*
  * for all email fields: use your own email

  After the install is done don't forget to save login name and password plus all info that came in the email



### FTP account creation

1. Login with cPanel

2. Choose "FTP Accounts"

3. As login name use the name of the subdomain (*note: this naming standard is new and may not be the same for all other ftp accounts that can be seen in the list below the create fields*)



### Wordpress setup

Prerequisites: The neat skype status v2/pro file

For the changes in this part we are assuming that we start from the admin panel http://{domain_name}/wp-admin/

Don't forget to save changes to settings!


#### Plugins

##### p2p

Install "posts 2 posts" by searching for the plugin under "add plugins"

##### Neat skype status pro/v2

Install neat skype status pro/v2 *from file* (ask SunyataZero if you don't have this)

#### Settings

1. settings -> neat skype status pro
  * Visible name: set to "empathizer!" ("Call " will be prepended to the name)
  * activate "initial check"

2. settings -> discussion
  * Uncheck "Allow people to post comments on new articles"

3. settings -> general
  * Check "Anyone can register"

4. settings -> permalink settings
  * Choose "Post name"


#### Adding the pages

Pages -> Add new

Please note: You will not see changes until the Empathy App plugin has been uploaded

Title | Shortcode (enter into page body after switching to "text" mode)
--- | ---
Home | [skype skypenames="echo123, infinitytaal"]
Email form | [ea_email_form]
Email sent | [ea_email_sent]
Donation form | [ea_donation_form]
Donation sent | [ea_donation_sent]


#### Customizing the appearance

1. Appearance -> Customize -> Static front page -> A static page -> Front page -> Home

2. Appearance -> Customize -> Widgets
  * Remove everything except for "meta"
  * Add "Pages", sort by page id

(Don't forget to save & publish)


### Uploading the EmpathyApp plugin

Please see [[Installing or upgrading the Empathy App plugin]]

An alternative way to install (requires an ftp account):

1. Upload all files (if you are using Netbeans (or probably many other IDEs) this can be done from there
  * Directory: /public_html/{name_of_subdomain}/wp-content/plugins/empathy_app
    * The path is important because when installing in the way above and when an automatic installation is done the "empathy_app" directory is chosen automatically
    * **Important: The directory name has been changed from "empathyapp" to "empathy_app", please update your developer path if you are using the old path**
2. Go to the wp admin area, then choose Plugins, and activate
  If there are problems with any of these two steps (often is unforturnately):
  1. Upload the plugin source again (some directories may not have been created)
  2. Refresh the plugin page and try activating the plugin again

***

#### Appendix A: Creating new users

This can be done by going to Users -> Add new, and then choosing role: admin, and activate the checkbox "email password to new user"

If you didn't install yourself, ask the person who installed wp to create an admin account


#### Appendix B: Uninstalling the plugin

TODO

Simple version: Disable the plugin and remove all the files

Removing the files will not remove db tables