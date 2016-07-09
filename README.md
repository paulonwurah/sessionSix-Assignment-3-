1.Find the five longest movies according to their duration 

val Input  = sc. textFile (movie.txt)

val InputSplit = Input.map(x => x.split(“,”))

val mapInput = InputSplit.map(x => (x,x.last.toDouble))

val sort = mapInput.sortBy(_._2,false)

val output = sort.take(5)

output.collect()

2.Find the top 5 rated movies in the year 1995

val Input  = sc. textFile (movie.txt)

val InputSplit = Input.map(x => x.split(“,”))

val filterInput = InputSplit.filter(x  => x.contains(“1995”))

val mapInput = filterInput.map(x => (x,x(3))

val sortInput = mapInput.sortBy(_._2,false)

val output = sortInput.take(5)

output.collect()



  
