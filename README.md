class selenium.webdriver.firefox.options.Log¶
Bases: object

### __init__()
x.__init__(…) initializes x; see help(type(x)) for signature

### to_capabilities()
class selenium.webdriver.firefox.options.Options
Bases: object

### __init__()
x.__init__(…) initializes x; see help(type(x)) for signature

### add_argument(argument)
Add argument to be used for the browser process.

### set_capability(name, value)
Sets a capability.

### set_headless(headless=True)
Deprecated, options.headless = True

### set_preference(name, value)
Sets a preference.

### to_capabilities()
Marshals the Firefox options to a moz:firefoxOptions object.

### KEY = 'moz:firefoxOptions'
accept_insecure_certs
### arguments
Returns a list of browser process arguments.

###binary
Returns the FirefoxBinary instance

###binary_location
Returns the location of the binary.

### capabilities
headless
Returns whether or not the headless argument is set

###preferences
Returns a dict of preferences.

###profile
Returns the Firefox profile to use.

###proxy
returns Proxy if set otherwise None.
