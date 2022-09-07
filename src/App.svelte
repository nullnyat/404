<script lang="ts">
    import './assets/style.sass'
    import qrCode from './assets/QR.png'

    let count = 0
    setInterval(countUp, 30);

    function countUp() {
        count = Math.min(100, count + 1)
    }
</script>

<template lang="pug">
    h1 :(
    p.RedirectMessage このページは存在しないよ。5秒後にホームページに移動するよ。
    p.count {count}%完了
    .entire
        img(src='{qrCode}' alt='QR')
        div
            .list
                a(href='https://nullc.at') https://nullc.at
                p 停止コード: 404
                p 失敗した内容: PAGE_NOT_FOUND
</template>
