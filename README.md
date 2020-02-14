# CalendarEvents-Reader
Livecode Builder Library that reads Calendar Event data (Mac OS)
A first attempt at a Library to read MacOS calendar events.  Provides Livecode Script with two commands, for example

put smkCheckAuth() into tAuthStatus

   if tAuthStatus is "Authorised" then
   
      put smkGetListOfEvents("2019-01-01","2020-02-07") into tArray
      
   else
   
      answer "Error, You need to grant permission for this application to access Calendars."
      
   end if
   
   
It is read only i.e. there is no way to edit or create new events.  The code is does not work on iOS as it uses the older depreciated -init method as I have not worked out how to wrap the new one because it employs a Block callback.
