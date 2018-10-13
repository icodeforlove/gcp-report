# gcp-report

allows simple error reporting for "Stack Driver: Error Reporting"

```
import gcpReport from 'gcp-report';

const report = gcpReport({
    // enable this to automatically report uncaught errors
    catchUncaughtErrors: true,

    service: 'service-name', // option (default "node")
    version: '0.0.1'// optional (default "latest")
});

report(new Error('test')).then(() => {
    // done reporting error
});
```