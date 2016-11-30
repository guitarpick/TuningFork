![](header.png)

### Overview
[![Build Status](https://travis-ci.org/comyarzaheri/TuningFork.svg?branch=master)](https://travis-ci.org/comyar/TuningFork)
[![Version](http://img.shields.io/cocoapods/v/TuningFork.svg)](http://cocoapods.org/?q=TuningFork)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/comyar/TuningFork)
[![License](http://img.shields.io/cocoapods/l/TuningFork.svg)](https://github.com/comyar/TuningFork/blob/master/LICENSE)
[![git-brag-stats](https://labs.turbo.run/git-brag?user=comyar&repo=TuningFork)](https://github.com/comyar/TuningFork)

TuningFork is a simple utility for processing microphone input and interpreting pitch, frequency, amplitude, etc. 

TuningFork powers the [Partita](https://github.com/comyar/Partita) instrument tuner app.

# Usage 

### Quick Start

##### CocoaPods

Add the following to your Podfile:

```ruby
pod 'TuningFork'
```
##### Carthage 

Add the following to your Cartfile:

```ruby
github "comyarzaheri/TuningFork" "master"
```

### Using a Tuner

```swift
import TuningFork

class MyTunerDelegate: TunerDelegate {
	func tunerDidUpdate(tuner: Tuner, output: TunerOutput) {
		// Dreams come true here
		print(output.pitch, output.octave) 
	}
}

let tuner = Tuner()
let delegate = MyTunerDelegate()
tuner.delegate = delegate
tuner.start()
```

# License 

TuningFork is available under the [MIT License](LICENSE).

# Contributors

* [@comyar](https://github.com/comyar)
