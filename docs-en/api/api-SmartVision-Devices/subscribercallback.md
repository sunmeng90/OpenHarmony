# SubscriberCallback<a name="EN-US_TOPIC_0000001055358146"></a>

## **Overview**<a name="section1285193163093537"></a>

**Related Modules:**

[Core](core.md)

**Description:**

Called when the driver subscribes to other driver services. 

The callback is used in the service subscription mechanism. After the driver is registered with the HDF, the HDF proactively invokes the callback after the subscribed-to driver is loaded.

**Since:**

1.0

## **Summary**<a name="section2089491515093537"></a>

## Data Fields<a name="pub-attribs"></a>

<a name="table752331507093537"></a>
<table><thead align="left"><tr id="row538456016093537"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="p894061631093537"><a name="p894061631093537"></a><a name="p894061631093537"></a>Variable Name</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="p176688710093537"><a name="p176688710093537"></a><a name="p176688710093537"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="row841537040093537"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p831597522093537"><a name="p831597522093537"></a><a name="p831597522093537"></a><a href="subscribercallback.md#af8640bdb30eb50c1d69781940b62c20d">deviceObject</a></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p559955705093537"><a name="p559955705093537"></a><a name="p559955705093537"></a>struct <a href="hdfdeviceobject.md">HdfDeviceObject</a> * </p>
</td>
</tr>
<tr id="row1931952046093537"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p404291654093537"><a name="p404291654093537"></a><a name="p404291654093537"></a><a href="subscribercallback.md#a71a9efad360e2944550c36a97791e6e6">OnServiceConnected</a> )(struct <a href="hdfdeviceobject.md">HdfDeviceObject</a> *<a href="subscribercallback.md#af8640bdb30eb50c1d69781940b62c20d">deviceObject</a>, const struct <a href="hdfobject.md">HdfObject</a> *service)</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p398432468093537"><a name="p398432468093537"></a><a name="p398432468093537"></a>int32_t(* </p>
<p id="p776445754093537"><a name="p776445754093537"></a><a name="p776445754093537"></a>Called by the HDF when the subscribed-to driver service is loaded. </p>
</td>
</tr>
</tbody>
</table>

## **Details**<a name="section616046405093537"></a>

## **Field Documentation**<a name="section1843561605093537"></a>

## deviceObject<a name="af8640bdb30eb50c1d69781940b62c20d"></a>

```
struct [HdfDeviceObject](hdfdeviceobject.md)* SubscriberCallback::deviceObject
```

 **Description:**

Driver object of the subscriber 

## OnServiceConnected<a name="a71a9efad360e2944550c36a97791e6e6"></a>

```
int32_t(* SubscriberCallback::OnServiceConnected) (struct [HdfDeviceObject](hdfdeviceobject.md) *[deviceObject](subscribercallback.md#af8640bdb30eb50c1d69781940b62c20d), const struct [HdfObject](hdfobject.md) *service)
```

 **Description:**

Called by the HDF when the subscribed-to driver service is loaded. 

**Parameters:**

<a name="table928045324093537"></a>
<table><thead align="left"><tr id="row217821336093537"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="p1688619299093537"><a name="p1688619299093537"></a><a name="p1688619299093537"></a>Name</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="p1403642094093537"><a name="p1403642094093537"></a><a name="p1403642094093537"></a>Description</p>
</th>
</tr>
</thead>
<tbody><tr id="row620005864093537"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 ">deviceObject</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 ">Indicates the pointer to the variable of the <a href="hdfdeviceobject.md">HdfDeviceObject</a> type. This variable is generated by the HDF and passed to the driver. </td>
</tr>
<tr id="row2045330729093537"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 ">service</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 ">Indicates the pointer to the service object. </td>
</tr>
</tbody>
</table>

**Returns:**

Returns  **0**  if the operation is successful; returns a non-zero value otherwise.



