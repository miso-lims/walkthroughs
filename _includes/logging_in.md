{% if detailed == true %}
Much like the old Geospiza LIMS, you need to log in to MISO LIMS in order to
make changes to any LIMS entities. 
Logging in lets MISO record any changes you make on entities you have access to.

If you were able to log in to Geospiza LIMS, you already have the correct
permissions and can proceed to logging in. If you are a new user, you will need
to contact <helpdesk@oicr.on.ca> so that they put you into the appropriate
Active Directory group, `MISO_ROLE_INTERNAL`.

{% else %}
You need to log in to MISO LIMS in order to make changes to any LIMS entities. 
Logging in lets MISO record any changes you make on entities you have access to.
If you are a new user and have not been given a username and password, you 
will first need to get a username and password by following the steps in the
<a href="plain-0-0-admin-tasks#users">Adding Users</a> section.
{% endif %}

-----------

Try to log in now:

1. Click on <a href="{{ misoUrl }}"
target="\_new" >{{ misoUrl }}</a>.
1. Enter your
username (e.g. jdoe) and password and click the Login button.
{% if detailed == true %}
MISO uses the same username and password as your OICR email account.
{% endif %}

If all goes well, you should see the MISO Dashboard and see a message at the
top right: "Logged in as: **jdoe**".
