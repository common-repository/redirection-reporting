=== Redirection Reporting ===
Contributors: mrdenny
Donate Link: http://dcac.co/go/RedirectionReporting
Tags: reporting, redirection
Requires at least: 3.0.1
Tested up to: 6.6.1
Stable tag: trunk
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Allows for daily reporting for redirected requests.

== Description ==

Allows for more details reporting for the "Redirection" plugin by John Godley.  
This plugin will not do anything for you without using the Redirection plugin 
to handle your 301 redirections.  This plugin was built to fix a gap in the 
reporting which the Redirection plugin has.

== Installation ==

This section describes how to install the plugin and get it working.

e.g.

1. Upload `redirection-reporting.php` to the `/wp-content/plugins/redirection-reporting` directory
2. Activate the plugin through the 'Plugins' menu in WordPress
3. Configure the global settings through the settings page.


== Frequently Asked Questions ==

= What does this plugin do? =

This plugin simply reports on the redirection logs with day by day reporting.  It will also archive off data from the redirection_log table to redirection_log_archive (if enabled) to help keep the table that the redirection plugin writes to small.

= What date format should I be using? =

You should be able to use any date format.  The PHP is going to reformat it to the
way that MySQL wants to see it.

= Where do I find the reports? =

The "Redirection Reporting" link can be found under the tools menu, probably
right near the "Redirection" link.

= What is the archive feature for? =

When there are large amounts of data in the Redirection plugin's log table the pages 
which show the lists of available regex URLs can be slow to load as these come from 
the log table.  In order to make this load faster, on sites which have a very heavy 
workload the data from the log table can be archived.  This will not reduce the amount 
of data which is reported on as reports are run against the archive table and the 
normal table at the same time.

= After upgrading to v3.0 the reports don't work. =

On some systems the additional database objects which are needed are not being created.
In order to fix this, deactivate the plugin and reactivate it, or simply go to the settings 
page and click the "Save Settings" button.  We're working on making that a smoother upgrade.

== Screenshots ==

1. Normal URL report
2. The "RegEx Summary" report
3. Referrer Details report
4. Settings page


== Changelog ==

= 3.0.6 =
* Adjusting the view for reporting so that the columns are correct

= 3.0.5.1 =
* Fixed warnings on install or page review from PHP

= 3.0.5 =
* Fixed warnings on install or page review from PHP

= 3.0.4 =
* Tested for version 4.3

= 3.0.3 =
* Tested for version 4.1

= 3.0.2 =
* Fixed bug which prevented some users from logging in.

= 3.0.1 =
* Attempting to fix upgrade code to create database objects as needed.

= 3.0 =
* Added feature to archive off old redirection log data to another table within the database.
* Improved performace of loading RegEd selection lists (thanks for the archiving feature above).
* Major code cleanup, made the code much more managable for updating.

= 2.6.2 =
* Fixed Settings link from plugin page
* Added warning if Redirection plugin isn't installed or enabled.

= 2.6.1 =
* Added "Normal Summary" report to settings options
* Fixed "Normal Report" to settings options so that it is selected correctly on tools page.

= 2.6 =
* Code cleanup, moving code into multiple classes and multiple files.

= 2.5 =
* Added Normal Summary report to match the RegEx Summary report.

= 2.4 =
* Added blue icon file
* Fixed links on dates
* Removed blue "I" icon from date column
* Added ability to show date column on referrer details page or not based on setting

= 2.3 =
* Added ability to view details of what URLs are referring people by clicking the 
blue "I" icon when available.
* Added settings to trim the URLs which are displayed in the details report and to 
allow the user to specify if the report should open in a new tab or the same tab.

= 2.6.1 =
* Added "Normal Summary" report to settings options
* Fixed "Normal Report" to settings options so that it is selected correctly on tools page.

= 2.6 =
* Code cleanup, moving code into multiple classes and multiple files.

= 2.5 =
* Added Normal Summary report to match the RegEx Summary report.

= 2.4 =
* Added blue icon file
* Fixed links on dates
* Removed blue "I" icon from date column
* Added ability to show date column on referrer details page or not based on setting

= 2.3 =
* Added ability to view details of what URLs are referring people by clicking the 
blue "I" icon when available.
* Added settings to trim the URLs which are displayed in the details report and to 
allow the user to specify if the report should open in a new tab or the same tab.

= 2.2 =
* Added in a RegEx Summary report which allows you to show the total number of hits 
for all the URLs that match a specific RegEx entry for a specific date rate.  This 
is great for end of year reporting.

= 2.1 =
* Adding the ability to hide rollup values when they are available.

= 2.0 =
* Added settings screen.
* Allows setting of default report to show.
* Allows setting of default dates for reports to show.
* Available dates are Today, Yesterday, Two Days Ago, This Month.

= 1.9.1 =
* Fixed a typo in the code which caused the plugin users site to be unavailable.

= 1.9 =
* Added links from RegEx parent child report to normal RegEx report.
* Disabled report selection button when button isn't useful.
* Code cleanup.
* Fixed row by row colorization of report output

= 1.8 =
* Added in parent child style reporting for RegEx enabled URLs.  This allows you to report
on just the parent URL, but see the data for all the child values.
* Cleaned up the code, removed lots of duplicate code to make code maintenance easier.

= 1.7 =
* Added in reporting specific for RegEx enabled redirection URLs.  This report shows 
all available regex values and allows reports to be run for those specific values.
This report only works when redirection URLs are configured with the RegEx flag.

= 1.6 =
* Added the ability to report on all configured URLs in a single report for a date range.

= 1.1 =
* Fixed the FAQ and readme file.

= 1.0 =
* Created the report


== Upgrade Notice ==


