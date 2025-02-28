# Module simple-module 

The function of this module is to provide a determination of wether a person was detected in a given camera. If a person was detected the module will return 1 other wise it will return 0 in the attribute person_detected 

## Model jadorg:simple-module:simple-detection

This module relies on the model of a provided module. 

### Configuration

simple-module is simply relies on existing modules provide the camera vision and categories the image. So to use this module, one needs to: 
- follow the instructions to [add a camera from the Viam Registry]([https://docs.viam.com/operate/reference/components/camera/webcam/#:~:text=Navigate%20to%20the%20CONFIGURE%20tab,your%20camera%20and%20click%20Create.](https://docs.viam.com/operate/reference/components/camera/webcam/)
- follow the instrution to [add a sensor from the Viam Registry]
- Install simple-module from the registry
- Add the sensor as a dependency
- Update the following attribute template  to configure this model:

```json
{
  "camera": <string>,
  "detection_confidence": <float>,
  "sensor": <string>,
}```

Camera is the name of a camera component
Sensor is the name of a vision sensor which we want to choose
detection_confidence is the certainty between 0 and 1 that will determine if a person is recognized.

 
#### Attributes

The following attributes are available for this model:

| Name          | Type   | Inclusion | Description                |
|---------------|--------|-----------|----------------------------|
| `attribute_1` | float  | Required  | Description of attribute 1 |
| `attribute_2` | string | Optional  | Description of attribute 2 |

#### Example Configuration

```json
{
  "attribute_1": 1.0,
  "attribute_2": "foo"
}
```
