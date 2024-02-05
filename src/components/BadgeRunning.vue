<template>
    <span
        class="blink-running position-absolute text-dark top-0 start-100 translate-middle p-2 border border-dark rounded-circle border-3 hw-badge-50">
        <div class="hw-badge-20">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
                stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                class="feather feather-play-circle">
                <circle cx="12" cy="12" r="10"></circle>
                <polygon points="10 8 16 12 10 16 10 8"></polygon>
            </svg>
        </div>
    </span>
</template>

<script>
export default {
    name: 'BadgeRunning',
}
</script>