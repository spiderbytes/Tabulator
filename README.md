# Tabulator
SpiderBasic-Module to use the Tabulator-Library (http://olifolkerd.github.io/tabulator/)

![http://i.imgur.com/qDuf5H2.png](http://i.imgur.com/qDuf5H2.png)

## Demo

http://spiderbytes.tuebben.de/demos/Tabulator/

## Example

```
XIncludeFile "Tabulator.sbi"

Enumeration
	#myWindow
	#myTabulatorGadget
EndEnumeration

Procedure Main()
	
  OpenWindow(#myWindow, 0, 0, 1000, 600, "TabulatorDemo", #PB_Window_ScreenCentered)
  
  ContainerGadget(#myTabulatorGadget, 10, 10, WindowWidth(#myWindow) - 20, WindowHeight(#myWindow) - 20)
  CloseGadgetList()
  
  Protected Options
  
  ! v_options = {
  !   progressiveRender:true, //enable progressive rendering
  !   groupBy: 'gender',
  !   fitColumns: true
  ! }  
  
  Tabulator::BindGadget(#myTabulatorGadget, Options)
  
  Protected Columns
  
  ! v_columns = [
  !		{title:"Name", field:"name", width:200},
  !		{title:"Progress", field:"progress", width:100, sorter:"number"},
  !		{title:"Gender", field:"gender"},
  !		{title:"Rating", field:"rating", width:80},
  !		{title:"Favourite Color", field:"col"},
  !		{title:"Date Of Birth", field:"dob"},
  !		{title:"Driver", field:"car"},
  !	];
  
  Tabulator::SetAttribute(#myTabulatorGadget, Tabulator::#TabulatorColumns, Columns)
  
  Protected SampleData
  
  ! v_sampledata = [
  !		{id:1,  name:"Oli Bob",            progress:12,  gender:"male",   rating:1, col:"red",    dob:"",           car:1,      lucky_no:5},
  !		{id:2,  name:"Mary May",           progress:1,   gender:"female", rating:2, col:"blue",   dob:"14/05/1982", car:true,   lucky_no:10},
  !		{id:3,  name:"Christine Lobowski", progress:42,  gender:"female", rating:0, col:"green",  dob:"22/05/1982", car:"true", lucky_no:12},
  !		{id:4,  name:"Brendon Philips",    progress:100, gender:"male",   rating:1, col:"orange", dob:"01/08/1980",             lucky_no:18},
  !		{id:5,  name:"Margret Marmajuke",  progress:16,  gender:"female", rating:5, col:"yellow", dob:"31/01/1999",             lucky_no:33},
  !		{id:6,  name:"Frank Harbours",     progress:38,  gender:"male",   rating:4, col:"red",    dob:"12/05/1966", car:1,      lucky_no:2},
  !		{id:7,  name:"Jamie Newhart",      progress:23,  gender:"male",   rating:3, col:"green",  dob:"14/05/1985", car:true,   lucky_no:63},
  !		{id:8,  name:"Gemma Jane",         progress:60,  gender:"female", rating:0, col:"red",    dob:"22/05/1982", car:"true", lucky_no:72},
  !		{id:9,  name:"Emily Sykes",        progress:42,  gender:"female", rating:1, col:"maroon", dob:"11/11/1970",             lucky_no:44},
  !		{id:10, name:"James Newman",       progress:73,  gender:"male",   rating:5, col:"red",    dob:"22/03/1998",             lucky_no:9},
  !	];  
  
  Tabulator::SetAttribute(#myTabulatorGadget, Tabulator::#TabulatorData, SampleData)
  
EndProcedure

Tabulator::Init(@Main()) ; using standard-style (#Style_Tabulator)

; Tabulator::Init(@Main(), Tabulator::#Style_Bootstrap) ; using bootstrap-style
```