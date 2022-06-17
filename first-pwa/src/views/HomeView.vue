<template>
    <q-layout view="lHh Lpr lFf">
        <div class="q-pa-md row justify-center">
            <div style="width: 100%; max-width: 400px">
                <q-chat-message :text="['hey, how are you?']"
                                sent />
                <q-chat-message :text="['doing fine, how r you?']" />
            </div>
        </div>

    </q-layout>
</template>

<script>
    import { defineComponent, ref } from 'vue';
    export default defineComponent({
        name: 'HomeView',

        setup() {
            const leftDrawerOpen = ref(false);

            return {
                leftDrawerOpen,
                toggleLeftDrawer() {
                    leftDrawerOpen.value = !leftDrawerOpen.value;
                }
            };
        }
    });
</script>
