<template>
<div>
<div class="clipboard">
<button class="btn-clipboard" @click="copyClipboard()">copy</button>
</div>
<pre class="highlight">
<code>
box-shadow: {{itemsData.x}}px {{itemsData.y}}px {{itemsData.blur}}px {{itemsData.spread}}px {{itemsData.color}};
border-radius: {{itemsData.radius}}px;
</code>
</pre>
</div>
</template>

<script>
export default {
    name: 'clipboard',
    props: ['itemsData'],
    methods: {
        copyClipboard() {
            let code = document.querySelector('code').textContent;
            let textarea = document.createElement('textarea');
            textarea.textContent = code;
            document.body.append(textarea);
            textarea.select();
            document.execCommand('copy');
            document.body.removeChild(textarea);
        }
    }
}
</script>