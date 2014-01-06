knockout-dynamic-forms
======================
License: MIT

Knockout Dynamic Forms with Validation

With this code you can generate a form Dynamically based on a JSON file including validation.

JSON file markup (if a field is not required, just leave as an empty string or array):

        { "formElements": [
            {
                "Name"              : "Gender",                         // String: Name of field
                "Element"           : "input",                          // String: Element (Can be: input, textarea, button, select)
                "Type"              : "radio",                          // String: Type (Can be: text, radio, checkbox, hidden, password, submit)
                "Options"           : ["Male", "Female", "Unkown"],     // Array: Options (Used by select, radio, checkbox)
                "Placeholder"       : "",                               // String: A placeholder text
                "Value"             : "",                               // String/Integer: Default value 
                "HideField"         : {                                 // Set if a field needs to be hidden if the value of the current element
                                                                        // meets a certain condition
                    "HideElement"   : "",                               // String: The element (by name)  that needs to be hidden
                    "HideCondition" : ""                                // String/REGEX: The condition the value of the current element has to match
                },
                "Validation"        : {                                 // Form validation using kockout/validation. All options of KO/validation can be used.
                    "required"  : "This field is required",             // String/Boolean: Can be true/false or a string with the validation message
                    "minLength" : 1,                                    // Validation example
                    "maxLength" : 100,                                  // Validation example
                    "pattern"   : "^[A-Z0-9].$"                         // Validation REGEX example
                }
            }
        } 
        
The HTML generated uses YAML (http://www.yaml.de/) but ofcourse you can alter them.
Two stubs are included for testing purposes.

Feel free to improve or use. 
(ps, run on a webserver, locally does not work of course)
