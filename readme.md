v8-profiler provides [node](http://github.com/ry/node) bindings for the v8 
profiler and integration with [node-inspector](http://github.com/dannycoates/node-inspector)

## Installation

		npm install v8-profiler

## Usage

		var profiler = require('v8-profiler');

## API

#####Profiling
	
		profiler.startProfiling([name])                   //begin cpu profiling
		var cpuProfile = profiler.stopProfiling([name])   //finish cpu profiling
	
You can also save CpuProfile and then load it in to chrome for viewing. (tested on chrome >=v28)
>Save as {name}.cpuprofile then open in chrome via inspector->profile panel

		var cpuProfile = profiler.stopProfiling([name])   //finish cpu profiling
		cpuProfile.save(*filePath*)
	
#####Snapshots

Heap

		var snapshot = profiler.takeSnapshot([name])      //takes a heap snapshot



## node-inspector

Cpu profiles can be viewed and heap snapshots may be taken and viewed from the
profiles panel.
