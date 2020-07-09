# How to view the Bing map in WPF maps

This article explains how to show the external geospatial imagery resources for deep-zoom satellite viewing (Bing Map) in Syncfusion WPF map control as shown in below 

 ![Output image of BingMap](Output/BingMap.png)

 Please refer the below KB for more 

 [How to view the Bing map in WPF maps](https://www.syncfusion.com/kb/10799/?utm_medium=listing&utm_source=github-examples)

This can be achieved by using LayerType property in ImageryLayer as per below steps

**Step 1:** To enable this feature, define Bing as LayerType.

**Step 2:** Provide the bing Map Key to the BingMapKey property and that key has been obtained from the link.

**Step 3:** Provide the desired BingMapStyle from its available three types. they are,

1.	Aerial View
2.	Road View and
3.	AerialWithLabel View

Please refer the below code reference, for more details

[XAML]
```
        <syncfusion:SfMap>
            <syncfusion:SfMap.Layers>
                <syncfusion:ImageryLayer LayerType="Bing" BingMapKey="Your Bing Map Key " BingMapStyle="Aerial" />
            </syncfusion:SfMap.Layers>
        </syncfusion:SfMap>
```

[C#]

```
SfMap syncMap = new SfMap();
ImageryLayer imageryLayer = new ImageryLayer()
{
LayerType = LayerType.Bing,
BingMapKey = "Your Bing Map key",
BingMapStyle = BingMapStyle.Aerial,
};
syncMap.Layers.Add(imageryLayer);
```	

#See Also

[How to interact with shapes on SfMaps?](https://help.syncfusion.com/wpf/maps/map-selection)

[How to display item on a map?](https://help.syncfusion.com/wpf/maps/displaying-items-on-a-map)

[How to load multiple shape files on SfMaps?](https://help.syncfusion.com/wpf/maps/multilayer-support)

