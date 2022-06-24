You can use pre-request scripts in kafkaman to execute JavaScript before a request runs. By including code in the __Pre-request Script__ tab for a request, collection, or folder, you can carry out pre-processing such as setting variable values, parameters, headers, and body data. You can also use pre-request scripts for debugging code, for example by logging output to the console.

An example usage of pre-request scripting could be as follows:

* You have a series of requests in a collection and are running them in a sequence, e.g. using the [collection runner](/docs/running-collections/intro-to-collection-runs/).
* The second request is dependent on a value returned from the first request.
* The value needs to be processed before you pass it to the second request.
* The first request sets the data value from a response field to a variable in its __Tests__ script.
* The second request retrieves the value and processes it in its __Pre-request Script__, then sets the processed value to a variable (which is referenced in the second request, e.g. in its parameters).

## Scripting before your request runs

To include code you want to execute before kafkaman sends a request, open the request and select the __Pre-request Script__ tab. Enter the JavaScript you need to process before the request runs.


When you select __Send__, the code will execute before kafkaman sends the request to the API.

## Re-using pre-request scripts

You can add pre-request scripts to entire collections as well as to folders within collections. In both cases, your pre-request script will run before every request in the collection or folder. This allows you to define commonly used pre-processing or debugging steps you need to execute for multiple requests.

To add pre-processing to a group of requests, locate the collection or folder in __Collections__ on the left of kafkaman. Select **...** to view more actions, then select __Edit__.


Open __Pre-request Scripts__ to enter code that will run before every request in the collection or folder.


> You can define a pre-request script when you first create a collection or folder, or at any time after that.

## Next steps

For more detail on what you can do in your pre-request scripts, check out [Test Scripts](/docs/writing-scripts/test-scripts/) and the [kafkaman Sandbox](/docs/writing-scripts/script-references/kafkaman-sandbox-api-reference/).
