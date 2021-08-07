<template>
    <div>
        <h2>イベントのフォーム</h2>
        <label for="title">タイトル：</label>
        <input id="title" type="text" v-model="eventData.title">
        <p>タイトルの内容：{{eventData.title}}</p>
        <label for="maxNumber">最大人数：</label>
        <input id="maxNumber" type="number" v-model.number="eventData.maxNumber">
        <p>最大人数の内容：{{eventData.maxNumber}}</p>
        <label for="host">主催者：</label>
        <input id="host" type="text" v-model.trim="eventData.host">
        <p>主催者の内容：{{eventData.host}}</p>
        <label for="textarea">テキストエリア：</label>
        <textarea id="detail" cols="30" rows="10" v-model="eventData.detail"></textarea>
        <pre>テキストエリアの内容：{{eventData.detail}}</pre>
        <label for="isPrivate">非公開</label>
        <input type="checkbox" id="isPrivate" v-model="eventData.isPrivate">
        <p >{{eventData.isPrivate}}</p>
    </div>
</template>

<script>
export default {
        data() {
            return{
            eventData:{
                title: "タイトル",
                maxNumber: 0,
                host: "",
                detail: "",
                isPrivate: false
            },
        }
    }
}
</script>