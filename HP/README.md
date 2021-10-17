#  Horizon detection

The objective of Horizon Detection is to determine a set of distinctly visible boundaries on seismic data, that correspond to drastic changes in rock properties. In this task, we want to extend a sparse carcass of a horizon onto the whole field range.

## Data:

Participants are provided with a SEG-Y cube and a sparce labeled horizon in a CHARISMA format. The objective is to create labeling for entire field and submit produced picking in CHARISMA format for [evaluation](http://hackathon.eage-annual-amsterdam.org:8080).


* Examples
	- [SEG-Y file with seismic data](./data/demo_cube.sgy)
	- [CHARISMA csv-like file with carcass labeling](./data/carcass_0.char)
	- [CHARISMA csv-like file with horizon labeling](./data/horizon_0.char). Note that the only difference of this to a carcass is in field coverage.


## Submission process:

To submit results one should generate a charisma file with three columns: the first one corresponding to iline, second - crossline, and the last one should contain predicted horizon depth. See a [sample submission file](./data/horizon_0.char).

When the file is created and properly formatted, one should go to a [scorer site](http://hackathon.eage-annual-amsterdam.org:8080/), select `HP` task,  upload the file in the form and click `Submit` button.


## Metric:

The metric used to score participants' submits is mean absolute difference between predictions and expert labeling for the same horizons.
