# sales-temperature-v3-impala-udaf

Implemented - "uda-sample.cc","uda-sample.h","uda-sample-test.cc"

AvgSalesVolumeInit
AvgSalesVolumeUpdate
AvgSalesVolumeMerge
AvgSalesVolumeSerialize
AvgSalesVolumeFinalize


Represent day of month as 32bit variable "day_bit_mask" of AvgSalesVolumeStruct.
(e.g) 0b101000...  means 1st and 3rd day.
: In case target bit(corresponding a day) is not set with '1'-value,
set the bit as 1 and then increase "count" of AvgSalesVolumeStruct.
: If not ignore iteration.
(Note)."sum" of AvgSalesVolumeStruct might be added always.
