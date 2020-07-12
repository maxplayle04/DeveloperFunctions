# Release 0.1
Initial Commit 

# Release 0.2
- Fixed a bug involving dfConsole.writeProcessWithInformation([any varient of perams]) where the console colour would not correctly reset after the function had finished, 
leading to black text being printed after the function had finished. This was personally annoying me, so I assume it had been annoying at least one other person, my apologies.
- Updated writeProcessInformation to allow for input perams of: dfConsole.writeProcessInformation(string message, string source, ConsoleColor color);
- Added a light-weight version of Error Management to Developer Functions, allowing for better integration of the two libraries. A seperately downloadable version of EM will also
be available, which will be more feature-rich.
- Added a configuration element to the dfconfig.json of ErrorManagement/addWhittyComments, this controls whether the Error Management output should inclue a little joke amongst
the data for your error (this will not get in the way) (this will be true by default)
- Updated startup procedure, pulling new Error Management configuration objects.
- Added functions DeveloperFunctions.ErrorManagement.PrintErrorInformation with the following combenations of perams:
  - PrintErrorInformation(EMExceptionData exceptionData)
  - PrintErrorInformation(string ExceptionName, string ExceptionStackTrace, string ExceptionMessage)
  - PrintErrorInformation(Exception data)
- Added Type 'EMExceptionData' which can hold data about Exceptions without transmitting the exception (can also accept regular string inputs for sending to EM without actually throwing an exception) 
