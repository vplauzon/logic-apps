# Handling recursion in Logic Apps

This project shows how to handle recursion in a Logic App.  We explore two ways.

See the [following article](todo) for details.

## Parent-Child

Using two Logic App to get around the constraint of not self-calling.

To Deploy:

[![Deploy button](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https:%2F%2Fraw.githubusercontent.com%2Fvplauzon%2Flogic-apps%2Fmaster%2Frecursion%2Fparent-child%2Fdeploy-parent-child.json)

## Flat

Flattens the recursion, i.e. running everything in one Logic App instance using *Until* control.

To Deploy:

[![Deploy button](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https:%2F%2Fraw.githubusercontent.com%2Fvplauzon%2Flogic-apps%2Fmaster%2Frecursion%2Fflat%2Fdeploy-flat.json)