# sales-temperature-v3-impala-udaf

<p>Implemented - "uda-sample.cc","uda-sample.h","uda-sample-test.cc"

- AvgSalesVolumeInit</br>
- AvgSalesVolumeUpdate</br>
- AvgSalesVolumeMerge</br>
- AvgSalesVolumeSerialize</br>
- AvgSalesVolumeFinalize</br>


Represent day of month as 32bit variable "day_bit_mask" of AvgSalesVolumeStruct. </br>
(e.g) 0b101000...  means 1st and 3rd day. </br>
: In case target bit(corresponding a day) is not set with '1'-value,</br>
set the bit as 1 and then increase "count" of AvgSalesVolumeStruct.</br>
: If not ignore iteration.</br>
(Note)."sum" of AvgSalesVolumeStruct might be added always.</br>
