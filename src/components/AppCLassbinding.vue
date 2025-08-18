<template>
    <div>
        <h1>App Class Binding Example</h1>
        <p>This component demonstrates how to use class binding in Vue.js.</p>

        <div class="contain" :class="{ active: isActive, 'text-large': isLarge }">
            This text will change class based on the component's data properties.
        </div>
       
        <div >
            <p class="container">Lorem ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis quia quasi hic atque ab! Autem a velit cupiditate voluptatibus dolorem.</p>
        </div>
    </div>
</template>

<script>
import { ref, reactive } from 'vue';
export default {
    name: 'AppClassbinding',
    setup() {
        const isActive = ref(false);
        const isLarge = ref(false);
        const isvisible = ref(false);

        const container=reactive({
            color: 'blue',
            fontSize: '16px',
            backgroundColor: 'red'
        })

        function toggleActive() {
            isActive.value = !isActive.value;
        }

        function toggleSize() {
            isLarge.value = !isLarge.value;
        }

        function isshow() {
            isvisible.value = !isvisible.value;
        }

        return {
            isActive,
            isLarge,
            toggleActive,
            toggleSize,
            isshow,
            isvisible,
            container
        };
    }
};
</script>

<style scoped>
.active {
    color: green;
}

.text-large {
    font-size: 20px;
}

.visible {
    display: block;
}

.hide {
    display: none;
}

.contain {
    padding: 20px;
    border: 1px solid #ccc;
    margin-bottom: 20px;
}
</style>