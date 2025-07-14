
## Overview

mobilevitals.org is an effort, inspired by [Web Vitals](https://web.dev/articles/vitals), to define similar quality signals for mobile development. With the goal of helping app developers deliver a great mobile user experience, regardless of whether you're building for iOS, or Android.

We've used benchmarks collected from real-world applications to help set goals for these metrics. Answering the question, _"what *is* a good experience on my platform?"_

## The Metrics

### Cold Start

The time it takes a mobile application to start either immediately after booting,
or after the application has been killed or evicted from memory.

#### Why is this important?

Cold Start repsresents a users first experience with your application. Make a good first impression.

#### How to Measure

##### Android

[//]: # "prompt(cursor): replace this with a description of how to measure cold start on an android device with syntax highlighted code samples."

##### iOS

[//]: # "prompt(cursor): replace this with a description of how to measure cold start on an iOS device with syntax highlighted code samples."

#### Thresholds

##### Android

* `good`: 200ms - 1s.
* `meh`: 1s - 3s.
* `bad`: >3s.

##### iOS

* `good`: 200ms - 1s.
* `meh`: 1s - 3s.
* `bad`: >3s.

### Warm Start

Warm Starts measure how long it takes your application to start when some combination of
state and resources is already available in memory. Warm start measures a spectrum of
behaviour, as it depends on what resources are available, vs., what's been evicted.

#### Why is this important?

Your users will frequently not be launching your application from
scratch. Slow Warm Start performance will contribute to bad perceived performance over time.

#### How to Measure

##### Android

[//]: # "prompt(cursor): replace this with a description of how to measure warm start on an android device with syntax highlighted code samples."

##### iOS

[//]: # "prompt(cursor): replace this with a description of how to measure warm start on an iOS device with syntax highlighted code samples."

#### Thresholds

##### Android

* `good`: 200ms - 1s.
* `meh`: 1s - 3s.
* `bad`: >3s.

##### iOS

* `good`: 200ms - 1s.
* `meh`: 1s - 3s.
* `bad`: >3s.

### Time to Initial Display

The time it takes your application, either from a cold or warm start, to render its
first frame of animation to screen.

#### Why is this important?

This metric is a good indicator of when your user perceives your application as having actually launched.

#### How to Measure

##### Android

[//]: # "prompt(cursor): replace this with a description of how to measure Tim to Initial Display on an android device with syntax highlighted code samples."

##### iOS

[//]: # "prompt(cursor): replace this with a description of how to measure Time to Intiial Display on an iOS device with syntax highlighted code samples."

#### Thresholds

##### Android

* `good`: 200ms - 1s.
* `meh`: 1s - 3s.
* `bad`: >3s.

##### iOS

* `good`: 200ms - 1s.
* `meh`: 1s - 3s.
* `bad`: >3s.

### Time to Full Display

The time it takes your application to actually become useable.

#### Why is this important?

If additional work, e.g., [rendering a document](https://developer.apple.com/documentation/xcode/reducing-your-app-s-launch-time#Track-additional-startup-activities), needs to happen before
your application becomes useable, this will contribute to your users perceived performance.

#### How to Measure

##### Android

[//]: # "prompt(cursor): replace this with a description of how to measure Time to Full Display on an android device with syntax highlighted code samples."

##### iOS

[//]: # "prompt(cursor): replace this with a description of how to measure Time to Full Display on an iOS device with syntax highlighted code samples."

#### Thresholds

##### Android

* `good`: 200ms - 1s.
* `meh`: 1s - 3s.
* `bad`: >3s.

##### iOS

* `good`: 200ms - 1s.
* `meh`: 1s - 3s.
* `bad`: >3s.

### Frame Delay

When a user intercts with your application, the next frame of animation should render in a
reasonable amount of time and, the app falling back into a responsive state.

Frame delay is a spectrum, slow frames _feel_ janky, where as truly frozen frames can result
in an application feeling unresponsive or hung.

#### Why is this important?

A janky or frozen application feels unstable and, in general, is a bad user experience.

#### How to Measure

##### Android

[//]: # "prompt(cursor): replace this with a description of how to measure render delay on an android device with syntax highlighted code samples."

##### iOS

[//]: # "prompt(cursor): replace this with a description of how to measure render delay on an iOS device with syntax highlighted code samples."

#### Thresholds

##### Android

* `good`: 200ms - 1s.
* `meh`: 1s - 3s.
* `bad`: >3s.

##### iOS

* `good`: 200ms - 1s.
* `meh`: 1s - 3s.
* `bad`: >3s.

## Calculating Mobile Vitals Score

### Individual Metrics 

The `good`, `meh`, `bad` measurement for each individual metric is calculated based on the observed behaviour of Sentry’s corpus of mobile telemetry, along with other telemetry that has been provided by the community.

A score in the 8th percentile or higher, represents `good`, a score of 25th percentile or higher `meh`, and a score below the 25th percentile is `bad`.

Scores are further broken out by Android and iOS, as there’s significant variation between the two device types.

### Overall score

Similar to [lighthouse performance-scoring](https://developer.chrome.com/docs/lighthouse/performance/performance-scoring), the overall score provides a score between 1 and 100 for Mobile Vitals, based on a log-normal distribution of each weighted score.

Each individual score is weighted as follows, join the discussion in CONTRIBUTING if you’d like to help shape the weighting that’s applied (*this is a first pass, based on our best guesses).*

## Further Reading

### Cold Start / Warm Start

- ]iOS: Understand the cold and warm launch](https://developer.android.com/topic/performance/vitals/launch-time#cold).
- [Android: Understand the different app startup times](https://developer.android.com/topic/performance/vitals/launch-time#startup-state).

### Time to Initial Display

- [Android: Time to initial display](https://developer.android.com/topic/performance/vitals/launch-time#time-initial).
- [iOS: Track additional startup activities](https://developer.apple.com/documentation/xcode/reducing-your-app-s-launch-time#Track-additional-startup-activities).


### Time to Full Display

- [Android: Time to full display](https://developer.android.com/topic/performance/vitals/launch-time#time-full).
- [iOS: Track additional startup activities](https://developer.apple.com/documentation/xcode/reducing-your-app-s-launch-time#Track-additional-startup-activities).

### Frame Delay

- [Android: Relationship between Slow Frames, Frozen Frames, and ANR](https://developer.android.com/topic/performance/vitals/render).
- [iOS: Understand hangs](https://developer.apple.com/documentation/xcode/understanding-hangs-in-your-app#Understand-hangs).

### Performance Scores

- [Lighthouse performance scoring](https://developer.chrome.com/docs/lighthouse/performance/performance-scoring).
