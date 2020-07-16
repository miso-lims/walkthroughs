<a name="logging_in"/>

# 1. Logging in

You need to log in to MISO LIMS in order to make changes to any LIMS entities.
Logging in lets MISO record any changes you make on entities you have access to.

{% if include.detailed == true %}
If you are a new user, you will need
to contact <helpdesk@oicr.on.ca> so that they put you into the appropriate
Active Directory group, `MISO_ROLE_INTERNAL`.
{% else %}
If you are a new user and have not been given a username and password, you
will first need to get a username and password by following the steps in the
<a href="tutorial-plain-admin-tasks#users">Adding Users</a> section.
{% endif %}

-----------

Try to log in now:

1. Click on <a href="{{ site.miso_url }}"
target="\_new" >{{ site.miso_url }}</a>.
1. Enter your
username (e.g. jdoe) and password and click the Login button.
{% if include.detailed == true %}
MISO uses the same username and password as your OICR email account.
{% endif %}

If all goes well, you should see the MISO Dashboard and see a message at the
top right: "Logged in as: **jdoe**".
