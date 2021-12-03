<template>
    <div class="result" >
        <p> Reaction time: {{score}} ms</p> 
        <p class="rank">{{rank}}</p>
    </div>
</template>

<script>


export default {
    props: ['score'],
    data(){
        return{
            rank: null
        }
    },
    mounted() {
        if (this.score < 250 ) {
            this.rank = 'ninja'
        } else if (this.score < 400 ){
            this.rank = "rapid reflexes"
        } else {
            this.rank = 'too slow bro'
        }
    }
}
</script>

<style>
    .result{
        width: 150px;
        padding: 30px;
        border-radius: 20px;
        background: #1619b9;
        color: white;
        text-align: center;
        margin: 250px auto;

    }
    .rank{
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }



</style>