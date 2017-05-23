# Cloud IoT Core Python MQTT example

This sample app publishes data to Cloud Pub/Sub using the MQTT bridge provided
as part of Google Cloud IoT Core.

For detailed running instructions see the [MQTT code samples guide](https://cloud-dot-devsite.googleplex.com/iot/docs/protocol_bridge_guide).

# Setup

1. Use virtualenv to create a local Python environment.

    virtualenv env && source env/bin/activate

2. Install the dependencies

    pip install -r requirements.txt

# Running the Sample

The following snippet summarizes usage:

    cloudiot_mqtt_example.py [-h]
      --project_id PROJECT_ID
      --registry_id REGISTRY_ID
      --device_id DEVICE_ID
      --private_key_file PRIVATE_KEY_FILE
      --algorithm {RS256,ES256}
      [--cloud_region CLOUD_REGION]
      [--ca_certs CA_CERTS]
      [--num_messages NUM_MESSAGES]
      [--mqtt_bridge_hostname MQTT_BRIDGE_HOSTNAME]
      [--mqtt_bridge_port MQTT_BRIDGE_PORT]

For example, if your project ID is `blue-jet-123`, the following example shows
how you would execute using the configuration from the MQTT code samples guide:

    python cloudiot_mqtt_example.py \
      --registry_id my-registry \
      --project_id=blue-jet-123 \
      --device_id my-python-device \
      --algorithm RS256 \
      --private_key_file ../rsa_private.pem