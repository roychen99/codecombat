<template>
  <div class="classroom-body-view">
    <payment-student-license-purchase-component
      :price-info="priceInfo"
      :includes-text-array="includesTextArray"
      :payment-group-id="paymentGroupId"
    />
  </div>
</template>

<script>
import PaymentStudentLicensePurchaseComponent from "./PaymentStudentLicensePurchaseComponent";
export default {
  name: "PaymentSmallClassroomBodyView",
  components: {
    PaymentStudentLicensePurchaseComponent,
  },
  data() {
    return {
      includesTextArray: [
        'Full access to CodeCombat and Ozaria',
        'Customer support via email or chat'
      ]
    }
  },
  props: {
    priceInfo: {
      type: Object,
      required: true,
    },
    paymentGroupId: {
      type: String,
      required: true,
    },
  },
}
</script>

<style scoped lang="scss">
.classroom-body-view {
  padding-top: 20px;
  width: 40%;
  margin: auto;
}
</style>
