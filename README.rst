=========================
Facebook Application Tool
=========================


A command line tool to manage Facebook applications


Installing
__________

::
   $ pip3 install facebook-apps-tool


Config
_____

#. Create a config file on `~/.config/fbtool/config.yaml` and list your applications with the credentials:

 .. code-block:: yaml
     apps:
       my_great_app:
         app_id: 123123123123
         app_secret: S3cret
       another_great_app:
         app_id: 678678678
         app_secret: S3cret


#. Select the application you want to interact with:
   ::
      $ fbtool config use-app my_great_application

Usage
_____

#. list the existing commands:
   ::
      $ fbtool --help

#. Create test user on the selected application:
   ::
      $ fbtool test-users create --help

      Usage: fbtool test-users create [OPTIONS]

      You can create new test users

      Options:
      --quantity, --qty INTEGER  The quantity of tests users to create. (max 50)
                             [default: 1]
      --installed                Automatically installs the app for the test user
                             once it is created or associated.
      -n, --name TEXT            The name for the test user. When left blank, a
                             random name will be automatically generated.
      -perm, --permissions TEXT  List of permissions that are automatically
                             granted for the app when it is created or
                             associated.
      --help                     Show this message and exit.

      $ fbtool test-users create

      {
          "email": "wtoueqlxdl_1552022886@tfbnw.net",
          "id": "47837483748",
          "login_url": "https://developers.facebook.com/checkpoint/test-user-login/487387483847/",
          "password": "1713024715"
      }
