# LevelDB_Benchmark
A benchmark mixed YCSB key generator with standard db_bench

### what you need is to replace the old db_bench.cc with this one and  compiling .

#### new params: --benchmarks
    "fill_Zipsk,"         //fill db by Skewedzipfian-style key 
    "fill_ZipScr,"        //fill db by Scrambledzipfian-style key
    "fill_Uniform,"       //fill db by Uniform-style key
    "read&zipK,"          //read while fill db by Skewedzipfian-style key 
    "read&zipS,"          //read while fill db by Scrambledzipfian-style key
    "read&Uni,"           //read while fill db by Uniform-style key
    
#### other params used as usual

#### I also add Lantency info in this benchmarks,
     everytime you run fill_Zipsk , ZipScr or fill_Uniform, a lantency file will created in
     "/home/leveldb/LogDir/lantency_x.txt."(you can change the path by your need )
     The latency file describes latency（microsecond） per write_operation 
