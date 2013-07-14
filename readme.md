v8-profiler provides [node](http://github.com/ry/node) bindings for the v8 
profiler and integration with [node-inspector](http://github.com/dannycoates/node-inspector)

## Installation

		npm install v8-profiler

## Usage

		var profiler = require('v8-profiler');

## API

        var snapshot = profiler.takeSnapshot([name])      //takes a heap snapshot
        
        profiler.startProfiling([name])                   //begin cpu profiling
        var cpuProfile = profiler.stopProfiling([name])   //finish cpu profiling
        
        You can save CpuProfile and load in to chrome for viewing.
        *Save as {name}.cpuprofile then open in chrome via inspector->profile panel->Load*
        cpuProfile.save(*filePath*)
         
## node-inspector

Cpu profiles can be viewed and heap snapshots may be taken and viewed from the
profiles panel.
