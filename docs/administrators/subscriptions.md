# Subscribing to a feed for public calendars.

You probably want the incoming events to all be flagged with a specific category or categories. This can be useful for filtering.It makes it easier to include the calendar collections imported by the sync engine. Before carrying out the following steps ensure these categories are created.

For public events there are a few more options available when subscribing.

**Process Locations and Contacts:** This causes locations and contacts to be moved into x-properties **"X-BEDEWORK-LOCATION"** and **"X-BEDEWORK-CONTACT"**. The receiving end (bedework) may carry out further actions to validate the location or contact and as a result may set a preexisting location or contact in the event. The x-property is always available for display but this process allows the system to validate the location/contact.

**Process categories:** This does the same for categories.

### Note:
If you don't select those options then categories and locations will be created in bedework. This is probably not what is wanted as these are uncurated.

By setting the **Process....** flag you ensure that such locations and categories don't end up in the database.

**Suppress deletion of events?** This means that if events disappear from the feed they will stay in the database. This effectively turns the feed into a change feed adn can significantly reduce the size of the data. It does mean that events that MUST be deleted will require help from an administrator with sufficient privileges.
 
### Creating a public subscription

As a super user
  * Switch to the System tab and select "Manage calendars and folders".
  * Open up "public" and click the "+" on the cals folder.
  * Set the name - e.g "Athletics"
  * Check off categories for filtering
     * Click on "show/hide categories used for filtering"
     * Scroll down and select a previously created category or categories
  * Check off any categories you want applied on input -
    * Click on "show/hide categories for auto-tagging on input"
    * Scroll down and select a previously created category or categories
  * Mark as a subscription
  * Set the URL in the URl field
  * Set an id/password if necessary
  * Select the "Process Locations and Contacts" and "Process Categories" checkboxes if desired (probably so)
  * Set the location key field name for mapping locations
  * Set the refresh rate in minutes
  * Save

### Mapping Locations

The update process uses a key field set in locations to map the locations. The key field value should be an exact copy of what appears in the events.

The actual  location will be stored in an x-property