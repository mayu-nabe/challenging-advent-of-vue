<template>
    <div>
        <h1>Hoge View</h1>
        <div>
            <!-- {{ product.title[0] }} -->
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { useFetch } from '@vueuse/core'

const url = ref('/initial-url')

const { data, error } = useFetch(url)

// 再取得のトリガーになります
url.value = '/new-url'

// ToDo
    // お題を把握する
        // debounceについて
            // https://zenn.dev/ikefukurou777/articles/c9b21aba72d5df#%E5%AE%9F%E8%A3%85%E3%82%A4%E3%83%A1%E3%83%BC%E3%82%B8
        // 使用例
            // https://qiita.com/Thang_TQ/items/f8c0e9da93a457210d7d
    // 商品表示するところつくる
    // api取ってくる

    // 検索できるようにする
    // 検索時にdebounceを使う
    // 見た目を整える
</script>
