<script>

export default {
    name: "TextArea",
    data() {
        return {
            content: "",
        }
    },
    computed: {
      Lines(){
        return Array.from({ length: this.content.split("\n").length}, (_, i) => i += 1);
      },    
    },

    methods: {
        syncScroll(e){
            const textarea = e.target;
            const lineNumbers = this.$el.querySelector(".line-numbers");
            lineNumbers.scrollTop = textarea.scrollTop;
        },
    }
}

</script>

<template>
<div class="editor-area">
    <div class="line-numbers">
        <span v-for="line in Lines" :key="line">{{ line }}</span>
    </div>
    <textarea v-model="content" @scroll="syncScroll" class="editor" cols="30" rows="10" >


    </textarea>
</div>
</template>

<style scoped>

.editor-area{
    display: flex;
    width: 100%;
}

.line-numbers{
    display: flex;
    text-align: center;
    flex-direction: column;
    background-color: gray;
    overflow: hidden;
    user-select: none;
    border: 1px solid yellow;
    width: 3rem;
    height: 80vh;
}

.line-numbers span {
    display: block;
    text-align: center;
    justify-content: center;
    color: yellow;
}


textarea{
    width: 100%;
    height: 80vh;
    font-size: 16px;
    border: 1px solid yellow;
    color: white;
    outline: none;
    resize: none;
    background-color: rgb(41, 40, 40);
}

textarea:focus{
    border: 2px solid white;
}

</style>