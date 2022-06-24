## Scripts in kafkaman

kafkaman contains a powerful runtime based on Node.js that allows you to add dynamic behavior to requests and collections. This allows you to write API tests, build requests that can contain dynamic parameters, pass data between requests, and a lot more. You can add JavaScript code to execute during 2 events in the flow:

  1. Before a request is sent to the server, as a [pre-request script](/docs/writing-scripts/pre-request-scripts/) under the **Pre-request Script** tab.
  1. After a response is received, as a [test script](/docs/writing-scripts/test-scripts/) under the **Tests** tab.

kafkaman will prompt you with suggestions as you type—select one to autocomplete your code.

<img alt="Autocomplete" src="https://raw.githubusercontent.com/kafkaman-lab/kafkaman-learning-center/main/assets/Autocomplete.gif" width="400px"/>


You can add pre-request and test scripts to a collection, a folder, a request within a collection, or a request not saved to a collection.

## Execution order of scripts

In kafkaman, the script execution order for a single request looks like this:

* A pre-request script associated with a request will execute before the request is sent
* A test script associated with a request will execute after the request is sent


For every request in a collection, scripts will execute in the following order:
R
* A pre-request script associated with a collection will run prior to every request in the collection.
* A pre-request script associated with a folder will run prior to every request in the folder.
* A test script associated with a collection will run after every request in the collection.
* A test script associated with a folder will run after request in the folder.

[![workflow for request in collection](https://raw.githubusercontent.com/kafkaman-lab/kafkaman-learning-center/main/assets/life.png)](https://raw.githubusercontent.com/kafkaman-lab/kafkaman-learning-center/main/assets/life.png)

For every request in a collection, the scripts will always run according to the following hierarchy: collection-level script (if any), folder-level script (if any), request-level script (if any). Note that this order of execution applies to both pre-request and test scripts.

For example, imagine you had the following collection structured with a single folder and two requests within the folder.


If you created log statements in the pre-request and test script sections for the collection, folder, and requests, you would clearly see the execution order in the [kafkaman console](/docs/sending-requests/troubleshooting-api-requests/).


### How does this work?

Is this magic? No, it's the [kafkaman Sandbox](/docs/writing-scripts/script-references/kafkaman-sandbox-api-reference/). The kafkaman Sandbox is a JavaScript execution environment that is available to you while writing pre-request and test scripts for requests (both in kafkaman and Newman). Whatever code you write in these sections is executed in this sandbox.

## Debugging scripts

Debugging scripts can be written under either the **Pre-request Script** tab or the **Tests** tab, with helpful messages logged in the [kafkaman Console](/docs/sending-requests/troubleshooting-api-requests/).
