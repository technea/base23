# base23
Prime number
Problem-Solving in JavaScript: Sum of Prime Numbers



Recently, I practiced a classic JavaScript challenge: calculating the sum of all prime numbers up to a given number.



There are different approach you can follow and you can complete this challenge like looping Array.from but i have think loop and reduce is best way to do it

loop will do iteration and reduce will calcualte the sum

unction isPrime(n){
if(n<2) return false
for(let i=2; i<=Math.sqrt(n); i++){
if(n % i===0) return false
}
return true

}
// console.log(sumPrimes(10))
function sumPrimes(n){
let arr=[]
for(let i=2; i<=n; i++){
    if(isPrime(i)) { arr.push(i)
    }
}
return arr.reduce((acc,curr)=>acc+curr,0)
}
console.log(sumPrimes(10))
console.log(sumPrimes(100000))
