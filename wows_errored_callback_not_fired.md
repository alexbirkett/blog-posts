"Vows Errored » callback not fired

May 1, 2013

callback, Errored, node.js, uncaughtException, vows

When running vows tests, the cryptic “Errored » callback not fired” error message occurs when the process exits before all of the test callbacks are fired. This can happen if an unhanded exception occurs. Adding the following code to the test suite may help debug the problem:


    process.on('uncaughtException', function(err) {
        console.log('Caught exception: ' + err);
    });

If the exception that was throw is an instance of Error, the following code will show you where the error was thrown:


    process.on('uncaughtException', function(err) {
        console.log('Caught exception: ' + err.stack);
    });