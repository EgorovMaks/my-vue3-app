<template>
    <button class="base-button">
        {{ text }}
        <span v-if="arrow==='left'" class="base-button-arrow-left">
            <svg width="15" height="13" viewBox="0 0 15 13" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd" d="M11.9226 6.67278L0.570412 6.66773C0.257929 6.66759 0.00472069 6.41416 0.00485992 6.10168L0.00487518 6.09709C0.00757599 5.781 0.26404 5.52588 0.580147 5.52485L11.9083 5.48784L7.46464 1.01635C7.23486 0.785138 7.23115 0.412947 7.45628 0.177198C7.67473 -0.051569 8.03728 -0.0599298 8.26604 0.158525C8.26915 0.161493 8.27222 0.164496 8.27526 0.167534L13.8712 5.75744C14.0666 5.9526 14.0668 6.26918 13.8716 6.46455L13.87 6.4662L8.18914 12.1003C7.95859 12.329 7.58633 12.3275 7.35767 12.0969C7.35452 12.0937 7.3514 12.0905 7.34832 12.0873C7.11811 11.8443 7.12347 11.4621 7.36039 11.2257L11.9226 6.67278Z" fill="white" />
            </svg>
        </span>
    </button>
  </template>
  
  <script>
  export default {
    props: {
      text: {
        type: String,
        required: true,
      },
      arrow: {
        type: String,
        required: true,
      },
    },
  };
  </script>

  <style lang="scss" scoped>
    
    .base-button{
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 3px;
    padding: 9px 14px;
    font-size: 0.94rem;
    color: #fff;
    border-radius: 0.44rem;
    background: #0584fe;

    span{
        height: 19px;
    }
  }
</style>