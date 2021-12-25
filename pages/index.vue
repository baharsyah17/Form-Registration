<template>
  <div>
    <Registrasi
      :data-right="rightData"
      :form-left="leftForm"
      @onClick="submitData"
    />
  </div>
</template>

<script>
import Registrasi from "../components/organism/Registrasi.vue";
export default {
  components: { Registrasi },
  data() {
    return {
      rightData: {
        firstName: "",
        lastName: "",
        gender: "",
        email: "",
        phoneNumber: "",
        address: "",
        postalCode: "",
      },
      leftForm: {
        firstName: "",
        lastName: "",
        gender: "",
        email: "",
        phoneNumber: "",
        address: "",
        postalCode: "",
      },
    };
  },
  methods: {
    submitData() {
      this.rightData.firstName = this.leftForm.firstName;
      this.rightData.lastName = this.leftForm.lastName;
      this.rightData.gender = this.leftForm.gender;
      this.rightData.email = this.leftForm.email;
      this.rightData.phoneNumber = this.leftForm.phoneNumber;
      this.rightData.address = this.leftForm.address;
      this.rightData.postalCode = this.leftForm.postalCode;
    },
  },
};
</script>
