# ReScue: Crafting Regular Expression DoS Attacks

Usage:

```bash
java -jar rescue.jar <-sl string length> <-pz population size> <-g generations> 
					 <-cp crossover probability> <-mp mutation probability> regex
					 <-q> <-v>
```

Try to generate ReDoS string for `<regex>`. Default parameters: sl = 128, pz = 200, g = 200, cp = 10, mp = 10.

## Arguments

* `-h` Print help
* `-sl  ` Limit the string length
* `-pz` Limit the population size
* `-g`	Limit the generation
* `-cp` Set the crossover possiblity, the real possibility is calculated by cp / 100.0
* `-mp` Set the mutation possibility, the real possibility is calculated by mp / 100.0
* `-v`	View the inner structure of a regex
* `-q ` Quiet mode, do not show input message

## Examples

```
java -jar rescue.jar < "^h(i|ello), world$"
java -jar rescue.jar -sl 128 -pz 200 -g 200 -cp 10 -mp 10 < "^h(i|ello), world$"
```
