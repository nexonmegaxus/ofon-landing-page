<template>
    <NuxtLayout>
        <NuxtRouteAnnouncer />
        <NuxtLoadingIndicator color="#F25921" />
        <UNotifications />
        <NuxtPage />
    </NuxtLayout>
</template>

<style>
.page-enter-active,
.page-leave-active {
    transition: all 200ms;
}
.page-enter-from,
.page-leave-to {
    opacity: 0;
    filter: blur(0.5rem);
}
</style>

<script setup>
useHead({
    htmlAttrs: {
        lang: 'id',
    },
});
</script>
