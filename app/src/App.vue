<template>
  <div>
    <h1>Coding Hangman</h1>
    <h2>Choose the Number of letters</h2>
  <div id="display">{{ divContent }}</div>

    <button id = "choice4" >4 letters</button>
    <button id = "choice5" >5 letters</button>
    <button id = "choice6" >6 letters</button>
    <button id = "choice7" >7 letters</button>
    <button id = "choice8">8 letters</button>

    <button id ="clear" @click ="clearDiv">RESTART</button>

  </div>
</template>

<script setup>




const words =[ 
    { Word: 'math', Length: '4' },
    { Word: 'code', Length: '4' },
    { Word: 'loop', Length: '4' },
    { Word: 'style', Length: '5' },
    { Word: 'cache', Length: '5' },
    { Word: 'logic', Length: '5' },
    { Word: 'analog', Length: '6' },
    { Word: 'delete', Length: '6' },
    { Word: 'whalen', Length: '6' },
    { Word: 'hardware', Length: '7' },
    { Word: 'offline', Length: '7' },
    { Word: 'network', Length: '7' },
    { Word: 'computer', Length: '8' },
    { Word: 'debugger', Length: '8' },
    { Word: 'download', Length: '8' },

]



function display(words){




//end
const clearDiv = () => {
  divContent.value = ''; 
};

}
//hangman
//make 5  buttons with functions to display either 4,5,6,7,8 length words
//make a random index to choose one of the words
// correlate the button to the length of choice
//push the random word into another array
//create user input
//ask user to type letter
//if letter is found in the word show where that letter is in the array (display th letter)
// else if the letter is found but repeated, display , sorry you've chosen this letter already
// else( if it isn't found) save that letter in a spearte array (display)
// display the number of tries the user has used
//if the number of correct letter is = to world length , display the word and say congrats!

</script>

<style lang="scss" scoped>

</style>