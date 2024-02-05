<template>
    <span
        class="blink-idle position-absolute text-dark top-0 start-100 translate-middle p-2 border border-dark rounded-circle border-3 hw-badge-50">
        <div class="hw-badge-20">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none"
                stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                class="feather feather-clock">
                <circle cx="12" cy="12" r="10"></circle>
                <polyline points="12 6 12 12 16 14"></polyline>
            </svg>
        </div>
    </span>
</template>

<script>
export default {
    name: 'BadgeIdle',
}
</script>