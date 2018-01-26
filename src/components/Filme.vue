<template>

    <div class="gui-card" v-bind:style="efeitoClick" v-on:click="clickEfeito" v-on:mouseout="removeClickEfeito">
        <div class="gui-card__media">
            <img class="gui-card__img" v-bind:src="imagem" alt=""  />
        </div>
        <div class="gui-card__details">
            <div class="gui-card__title">
                {{titulo}}
            </div>
        </div>
    </div> 
  
</template>

<script>
    export default {
        name: 'teste',
        props: ['titulo', 'imagem'],
        data(){
            return{
                efeitoClick : null,
            }
        },
        methods: {
            clickEfeito: function(){
                console.log('clickEfeito')
                this.efeitoClick = 'transform: scale(1.9); margin-right: 100px;'
            },
            removeClickEfeito: function(){
                console.log('removeClickEfeito')
                this.efeitoClick = null;
            }
        }
    }
</script>

<style lang="scss">

h1{
    color: red
}

</style>
