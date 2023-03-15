# pwnagotchi
RogueAPDetector

The RogueAPDetector is a plugin for the Pwnagotchi that enhances its ability to detect and respond to rogue access points. The plugin uses machine learning algorithms to identify patterns in the access points the Pwnagotchi encounters and makes informed decisions about which access points are safe to connect to.

When a beacon is detected, the plugin extracts relevant data such as the SSID, MAC address, signal strength, encryption type, and whether the access point is hidden. This data is then added to a list of access points.

The plugin updates its model by converting the access point data into a matrix, which is clustered using KMeans. Outliers are detected using IsolationForest. The plugin then identifies potential rogue access points based on their cluster label and outlier score.

If a potential rogue access point is detected, the plugin sends a real-time alert to the Pwnagotchi, notifying the user of the potential threat. The plugin also offers options for mitigating the threat, such as blocking the access point or disconnecting from the network.

This plugin is intended for use in security applications, where it can help detect and respond to rogue access points in real-time. It can be customized to fit specific use cases, and its machine learning algorithms can be trained on new data to improve its accuracy over time.
