<template>
    <div>
        <h2>イベントのフォーム</h2>
        <label for="title">タイトル</label>
        <input id="title" type="text" v-model="eventData.title">
        <p>タイトルの内容：{{eventData.title}}</p>
        <label for="title">最大人数</label>
        <input id="title" type="number" v-model.number="eventData.title">
        <p>最大人数の内容：{{eventData.maxNumber}}</p>
    </div>
</template>

<script>
export default {
        data() {
            return{
            eventData:{
                title: "タイトル",
                maxNumber: 0
            },
        }
    }
}
</script>