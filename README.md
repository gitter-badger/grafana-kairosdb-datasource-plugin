grafana-kairosdb-datasource-plugin
==================================

This is a plugin that allows Grafana to support KairosDB as datasource.

To install past the files into the plugins directory of Grafana in a subfolder called kairosdb.

You can either use the provided configuration file or add the following to the existing configuration file:

        plugins: {
            // list of plugin panels
            panels: [],
            // requirejs modules in plugins folder that should be loaded
            // for example custom datasources
            dependencies: ['kairosdb/kairosdbDatasource'],
        }


and then specifiy the datasource:

        datasources: {
            kairosdb: {
                type: 'KairosDBDatasource',
                url: "http://"+window.location.hostname+":8080",
                default: true
            },
        },

This has been tested with release 1.8.1 (2014-09-30) of Grafana and will not necessarily work with older releases.
