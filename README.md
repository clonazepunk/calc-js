# calc-js
just another calculator...
/*Arreglar:
si apretás + 33 + 33 empieza a sumar strings
el segundo + (o cualquier signo) falla
si apretas +, dsp otro signo (con todos los signos) falla
*/

//var & const
/*var onOff = false;

const onButton = document.querySelector("#on");
onButton.addEventListener("dblclick", ()=>{
    onButton.classList.add("isOn");
    turnOnCalc(onOff);
console.log(onOff);

});
const offButton = document.querySelector("#off");
offButton.addEventListener("click",()=>{
    onButton.classList.remove("isOn");
    turnOffCalc(onOff);
console.log(onOff);

});

while(onOff){
    main();
}
*/
//function main(){
var screen = document.querySelector("#screen");
screen.value = 0;

const add = document.querySelector("#add");
add.addEventListener("click", toAdd);
const substract = document.querySelector("#substract");
substract.addEventListener("click", toSubstract);
const divide = document.querySelector("#divide");
divide.addEventListener("click", toDivide);
const multiply = document.querySelector("#multiply");
multiply.addEventListener("click", toMultiply);
const equal = document.querySelector("#eq");
eq.addEventListener("click", igual);

const buttonC = document.querySelector("#c");
c.addEventListener("click", clean);

const one = document.querySelector("#one");
one.addEventListener("click", () => {
    if (screen.value == 0) {
        screen.value = 1;
    }
    else {
        screen.value += 1;
    }
    //contAdd = 0, contSub = 0, contDiv = 0, contMul = 0;
});
const two = document.querySelector("#two");
two.addEventListener("click", () => {
    if (screen.value == 0) {
        screen.value = 2;
    }
    else {
        screen.value += 2;
    }
});
const three = document.querySelector("#three");
three.addEventListener("click", () => {
    if (screen.value == 0) {
        screen.value = 3;
    }
    else {
        screen.value += 3;
    }
});
const four = document.querySelector("#four");
four.addEventListener("click", () => {
    if (screen.value == 0) {
        screen.value = 4;
    }
    else {
        screen.value += 4;
    }
});
const five = document.querySelector("#five");
five.addEventListener("click", () => {
    if (screen.value == 0) {
        screen.value = 5;
    }
    else {
        screen.value += 5;
    }
});
const six = document.querySelector("#six");
six.addEventListener("click", () => {
    if (screen.value == 0) {
        screen.value = 6;
    }
    else {
        screen.value += 6;
    }
});
const seven = document.querySelector("#seven");
seven.addEventListener("click", () => {
    if (screen.value == 0) {
        screen.value = 7;
    }
    else {
        screen.value += 7;
    }
});
const eight = document.querySelector("#eight");
eight.addEventListener("click", () => {
    if (screen.value == 0) {
        screen.value = 8;
    }
    else {
        screen.value += 8;
    }
});
const nine = document.querySelector("#nine");
nine.addEventListener("click", () => {
    if (screen.value == 0) {
        screen.value = 9;
    }
    else {
        screen.value += 9;
    }
});
const zero = document.querySelector("#zero");
zero.addEventListener("click", () => {
    if (screen.value != 0) {
        screen.value = screen.value + "0";
    }
});

//AUX
var number = 0;
var acumulador = 0;
var auxA = 0;
var auxB = 0;
var type = "";
var contAdd = 0, contSub = 0, contDiv = 0, contMul = 0;

//Functions

function turnOnCalc(value) {
    value = true;
}
function turnOffCalc(value) {
    value = false;
}
function clean() {
    screen.value = "0";
    auxA = 0;
    auxB = 0;
    acumulador = 0;
}

function display() {

}

function toAdd() {
    if (contAdd < 1) {
        auxA = parseFloat(screen.value);
        type = "add";
        acumulador += auxA;
        contAdd++;
        screen.value = "";
    }

}
function toSubstract() {
    if (contSub < 1) {
        auxA = parseFloat(screen.value);
        type = "substract";
        acumulador -= auxA;
        contSub++;
        screen.value = "";
    }

}
function toDivide() {
    if (contDiv<1){
        auxA = parseFloat(screen.value);
        type = "divide";
        acumulador /= auxA;
        contSub ++;
        screen.value = "";
    }
    
}
function toMultiply() {
    if(contMul<1){
        auxA = parseFloat(screen.value);
        type = "multiply";
        acumulador *= auxA;
        contMul ++;
        screen.value = "";
    }
    
}
function igual() {
    auxB = parseFloat(screen.value);

    contAdd = 0, contSub = 0, contDiv = 0, contMul = 0;
    resolver();
}

function resolver() {
    if (type == "add") {
        screen.value = auxA + auxB;
    } else if (type == "substract") {
        screen.value = auxA - auxB;
    } else if (type == "divide") {
        screen.value = auxA / auxB;
    } if (type == "multiply") {
        screen.value = auxA * auxB;
    }
}

//}
