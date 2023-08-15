# Network Beaconing Detection

The Network Beaconing Detection package consists of a pivot transform required to stand up a framework to identify beaconing activity in your environment. The framework enables significant indicators of compromise (IoCs) for threat hunters and analysts to use as a starting point for an investigation in addition to helping them monitor network traffic for beaconing activities. 
This package requires a Platinum subscription. Please ensure that you have a Trial, Platinum, or Enterprise subscription before proceeding. This package is licensed under Elastic License 2.0..

## Installation

You can install the Network Beaconing Detection package via **Management > Integrations > Network Beaconing Detection**.

To inspect the installed assets, you can navigate to **Stack Management > Data > Transforms**.

| Transform name            | Purpose| 	Source index  |          Destination index                                                                           |
|---------------------------|--------|----------------|-------------------------------------------------------------------------|
| beaconing.pivot_transform |	Flags beaconing activity in your environment| 	logs-*        |	ml_beaconing_default|

## Dashboard

The **Network Beaconing Detection** has three set of dashboards namely - **Network Beaconing**, which is the main dashboard to monitor beaconing activity, **Beaconing Drilldown** to drilldown into relevant event logs and some statistics related to the beaconing activity, and finally, **Hosts Affected Over Time By Process Name** to monitor the reach of beaconing processes across hosts in your environment.

For the dashboards to work as expected, the following settings need to be configured in Kibana. 
1. Ensure the pivot transform is installed and running.
2. Go to **Management > Stack Management > Kibana > Data Views**. Click on **Create data view** button and enable **Allow hidden and system indices** under the **Show Advanced settings**.
3. Create a data view with the following settings:
    - Index pattern : `ml_beaconing_default`
    - Name: `ml_beaconing_default`
    - Custom data view ID: `ml_beaconing_default`
## Licensing
Usage in production requires that you have a license key that permits use of machine learning features.