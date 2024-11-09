<html>
<head>
    <meta charset="utf-8">
    <meta http-equiv="Content-Security-Policy" content="frame-ancestors 'self' *.force.com *.salesforce.com *.site.com">
    <title>Embedded Messaging</title>
</head>
<body>
    <!-- Embedded Messaging Bootstrap -->
    <script type='text/javascript'>
        function initEmbeddedMessaging() {
            try {
                embeddedservice_bootstrap.settings.language = 'en_US';
                
                // Add additional settings for iframe handling
                embeddedservice_bootstrap.settings.targetElement = '#embedded-messaging-container';
                embeddedservice_bootstrap.settings.enabledFeatures = ['LiveAgent'];
                embeddedservice_bootstrap.settings.entryFeature = 'LiveAgent';

                embeddedservice_bootstrap.init(
                    '00D8e000000T7Z5',
                    'MIAW_for_GitHub',
                    'https://cq-manufacturing-dev-ed.develop.my.site.com/ESWMIAWforGitHub1731141001903',
                    {
                        scrt2URL: 'https://cq-manufacturing-dev-ed.develop.my.salesforce-scrt.com',
                        allowedDomains: [
                            'cq-manufacturing-dev-ed--c.develop.vf.force.com',
                            '*.cq-manufacturing-dev-ed--c.develop.vf.force.com'
                        ]
                    }
                );
            } catch (err) {
                console.error('Error loading Embedded Messaging: ', err);
            }
        }
    </script>
    
    <!-- Container for the embedded messaging -->
    <div id="embedded-messaging-container"></div>

    <!-- Load the bootstrap script -->
    <script 
        type='text/javascript' 
        src='https://cq-manufacturing-dev-ed.develop.my.site.com/ESWMIAWforGitHub1731141001903/assets/js/bootstrap.min.js' 
        onload='initEmbeddedMessaging()'
        crossorigin="anonymous"
    ></script>
</body>
</html>
