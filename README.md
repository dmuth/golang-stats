## Golang Stats

This is a little package I wrote so that I could keep track of statistics and metrics in 
Google Go programs I developed.


### Installation

- Make sure your golib is set up properly:
   `export GOLIB=$HOME/golib`
- Now install the package
   `go get -v github.com/dmuth/glang-stats`


### Usage

    import stats "github.com/dmuth/golang-stats"

    //
    // Manipulate stats
    // The values will be initialized to zero if they do not already exist.
    //
    stats.IncrStat("key")
    stats.DercStat("key")
    stats.AddStat("key2", 3)
    stats.SubStat("key3", 4)

    //
    // Retrieve a stat
    //
    value := stats.Stat("key")
    
    //
    // Retrieve all stats as a map[string]int array
    //
    values := stats.StatAll()
    
    //
    // Write all stats to standard output once every 500 ms
    //
    stats.StatDump(.5)
    
    stats.StatDumpFunc(1, func(data map[string]int) {
      // Do something with our stats data once every second
    })


### Running the tests

    go test -v github.com/dmuth/golang-stats
    

### Contact

Questions?  Complaints?  Want to buy me drinks?

Here's my contact info: http://www.dmuth.org/contact

