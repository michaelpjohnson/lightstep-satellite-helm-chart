# Lightstep Satellite Helm Chart
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fmichaelpjohnson%2Flightstep-satellite-helm-chart.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fmichaelpjohnson%2Flightstep-satellite-helm-chart?ref=badge_shield)


This is a helm chart used to deploy a Lightstep satellite.  All configuration should be made in the values.yaml file.  Nothing else should need to be modified.  This does not include metrics monitoring and the extra containers of the StatsD exporter or endpoints.

Required Configuration:

The minimum configuration for this to work is for the user to input either a Satellite API key or point to a kubernetes secret that contains the Satellite API key.

If you're using an existing secret, enter the name and key of the secret that stores your satellite API key.  The values.yaml requires values for the secret name and secret key value, as below:

 > $ kubectl describe secret ${collector_satellite_key_secret_name}
 >
 > Name:         collector_satellite_key_secret_name
 >
 > Namespace:    default
 >
 > Labels:       <none>
 >
 > Annotations:  <none>
 >
 > Type:  Opaque
 >
 > Data
 > 
 > collector_satellite_key_secret_key:  390 bytes


Running the helm chart:

In order to install the helm chart, clone the project, input your satellite key (and any other configuration desired) and then run  `helm install satellite lightstep-satellite-helm-chart`, or match the file path to the directory you installed.

Or instal from artifact hub here: https://artifacthub.io/packages/helm/lightstepsatellite/lightstep



# Contributors

Please delete the charts/lightstepsatellite/README.md and regenerate it with the helm-docs (https://github.com/norwoodj/helm-docs) command.


## License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fmichaelpjohnson%2Flightstep-satellite-helm-chart.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fmichaelpjohnson%2Flightstep-satellite-helm-chart?ref=badge_large)