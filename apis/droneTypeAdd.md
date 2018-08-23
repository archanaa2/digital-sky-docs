# Drone Type/Model Add

API for admin to create drone type/model

**URL** : `/api/droneType`

**Method** : `POST`

**Auth required** : YES,

**Headers** : application/json, authentication: Bearer Token

**Data constraints**

```json
{
  "manufacturer": "[manufacturer of selected drone of type string obtained from drone details saved in the system]",
  "manufacturerAddress": "[manufacturer address of selected drone obtained from drone details saved in the system]",
  "manufacturerNationality": "[manufacturer nationality of selected drone obtained from drone details saved in the system]",
  "modelName": "[model name of selected drone obtained from drone details saved in the system of type string]",
  "modelNo": "[model no of selected drone obtained from drone details saved in the system of type string]",
  "serialNo": "[serial no of selected drone obtained from drone details saved in the system of type string]",
  "dateOfManufacture": "[date of manufacture of selected drone obtained from drone details saved in the system]",
  "wingType": "[wingType property of the selected drone which is an enum [FIXED, ROTARY]]",
  "maxTakeOffWeight": "[maxTakeOffWeight property of the selected drone as float]",
  "maxHeightAttainable": "[maxHeightAttainable property of the selected drone as float]",
  "compatiblePayload": "[compatiblePayload property of the selected drone as string]",
  "droneCategoryType": "[droneCategory property of the selected drone which is one of [MICRO, SMALL, MEDIUM, LARGE]]",
  "purposeOfOperation": "[purposeOfOperation property of the seleced drone as string]",
  "engineType": "[engineType property of selected drone as string]",
  "enginePower": "[enginePower property of selected drone as float]",
  "engineCount": "[engineCount property of selected drone as int]",
  "fuelCapacity": "[fuelCapacity property of selected drone as float]",
  "propellerDetails": "[propellerDetails property of selected drone as string]",
  "maxEndurance": "[max endurance property of selected drone as float]",
  "maxRange": "[max range property of selected drone as float]",
  "maxSpeed": "[max speed property of selected drone as float]",
  "maxHeightOfOperation": "[max height property of selected drone as float]",
  "dimensions": {
    "length": "[length of selected drone as float]",
    "breadth": "[breadth of selected drone as float]",
    "height": "[height of selected drone as float]"
  }
}
```

## Success Response

**Code** : `200 OK`

**Content example**

```json
{
  "id": 8,
  "modelName": "Beebop",
  "createdBy": 2,
  "createdDate": "23-08-2018",
  "lastModifiedBy": 2,
  "lastModifiedDate": "23-08-2018",
  "manufacturer": "Beebop",
  "manufacturerAddress": {
    "type": "DEFAULT",
    "lineOne": "House No",
    "lineTwo": "Street",
    "city": "Bangalore",
    "state": "Karnataka",
    "country": "India",
    "pinCode": "56089"
  },
  "manufacturerNationality": "Indian",
  "modelNo": "3222",
  "serialNo": "00001",
  "dateOfManufacture": "08-08-2008",
  "yearOfManufacture": null,
  "wingType": "Fixed",
  "maxTakeOffWeight": 400.0,
  "maxHeightAttainable": 500.0,
  "droneCategoryType": "MEDIUM",
  "compatiblePayload": "payload",
  "purposeOfOperation": "Recreational",
  "proposedBaseOfOperation": "Bangalore",
  "engineType": "Engine Type II",
  "enginePower": 4000.0,
  "engineCount": 2,
  "fuelCapacity": 4000.0,
  "propellerDetails": "some details",
  "dimensions": {
    "length": 4000.0,
    "breadth": 5000.0,
    "height": 1000.0
  },
  "maxEndurance": 300,
  "maxRange": 5000.0,
  "maxSpeed": 400.0,
  "hasGNSS": false,
  "maxHeightOfOperation": 1500.0,
  "opManualDocName": null,
  "maintenanceGuidelinesDocName": null
}
```

## Error Response

**Condition** : If provided with invalid payload

**Code** : `400 BAD REQUEST`


