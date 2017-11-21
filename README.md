# Interface-Connections
In order for this app to work you first must define the field that the connection information will be stored in using a rest client.

How to Create a Custom Attribute:<p>
Create a new Interface custom attribute which will be used to store the device logically connected to each interface in your Geo-Topology design
1. Use your favorite REST client ie. Chrome Postman REST client
2. Set the Request URL to: http://<da_host>:8581/rest/customattributedefinition
3. Add a content-type header: Content-Type application/xml
4. Set the request type to POST
5. Add the XML attribute definition below to the POST body
<CustomAttributeDefinition version='1.0.0'> <Label>Connects To</Label> <Description>Connects to Device</Description> <Hidden>false</Hidden>
<Storage> <AttributeName>ConnectsTo</AttributeName> <Type>String</Type> <ItemType>Port</ItemType>
</Storage> </CustomAttributeDefinition>
6. Send the POST to the Data Aggregator
7. Verify ‘200 Ok’ response

Download the Interface-Connections Zip file.<p>
Use the CAPC App Deployment feature to load the zip file.<p>
Add the app view to your devices interface context page.<p>
Navigate in CAPC to the interface and define the connection.<p>
