<template>
  <div class="md-layout">
    <md-card class="md-layout-item md-size-50 md-small-size-100">
      <md-card-header>
        <div class="md-title">{{ title }}</div>
      </md-card-header>

      <md-card-content>
        <div class="md-layout md-gutter">
          <div class="md-layout-item md-small-size-100">
            <md-field>
              <label for="first-name">First Name</label>
              <md-input name="first-name" id="first-name" v-model="form.firstName"/>
            </md-field>
          </div>

          <!--                    <div class="md-layout-item md-small-size-100">-->
          <!--                      <md-field :class="getValidationClass('lastName')">-->
          <!--                        <label for="last-name">Last Name</label>-->
          <!--                        <md-input name="last-name" id="last-name" autocomplete="family-name" v-model="form.lastName"-->
          <!--                                  :disabled="sending"/>-->
          <!--                        <span class="md-error" v-if="!$v.form.lastName.required">The last name is required</span>-->
          <!--                        <span class="md-error" v-else-if="!$v.form.lastName.minlength">Invalid last name</span>-->
          <!--                      </md-field>-->
          <!--                    </div>-->
        </div>

        <!--        <div class="md-layout md-gutter">-->
        <!--          <div class="md-layout-item md-small-size-100">-->
        <!--            <md-field :class="getValidationClass('gender')">-->
        <!--              <label for="gender">Gender</label>-->
        <!--              <md-select name="gender" id="gender" v-model="form.gender" md-dense :disabled="sending">-->
        <!--                <md-option></md-option>-->
        <!--                <md-option value="M">M</md-option>-->
        <!--                <md-option value="F">F</md-option>-->
        <!--              </md-select>-->
        <!--              <span class="md-error">The gender is required</span>-->
        <!--            </md-field>-->
        <!--          </div>-->

        <!--          <div class="md-layout-item md-small-size-100">-->
        <!--            <md-field :class="getValidationClass('age')">-->
        <!--              <label for="age">Age</label>-->
        <!--              <md-input type="number" id="age" name="age" autocomplete="age" v-model="form.age" :disabled="sending"/>-->
        <!--              <span class="md-error" v-if="!$v.form.age.required">The age is required</span>-->
        <!--              <span class="md-error" v-else-if="!$v.form.age.maxlength">Invalid age</span>-->
        <!--            </md-field>-->
        <!--          </div>-->
        <!--        </div>-->

        <!--        <md-field :class="getValidationClass('email')">-->
        <!--          <label for="email">Email</label>-->
        <!--          <md-input type="email" name="email" id="email" autocomplete="email" v-model="form.email"-->
        <!--                    :disabled="sending"/>-->
        <!--          <span class="md-error" v-if="!$v.form.email.required">The email is required</span>-->
        <!--          <span class="md-error" v-else-if="!$v.form.email.email">Invalid email</span>-->
        <!--        </md-field>-->
      </md-card-content>

      <md-card-actions>
        <md-button type="submit" class="md-primary">Register</md-button>
      </md-card-actions>
    </md-card>


    <!--    <md-card class="login-form">-->
    <!--      <md-app-toolbar class="md-primary md-dense md-layout md-alignment-center-space-between">-->
    <!--        <div class="md-layout-item md-title">-->
    <!--          {{ title }}-->
    <!--        </div>-->
    <!--      </md-app-toolbar>-->
    <!--      <div id="padder">-->
    <!--        <md-datepicker v-model="selectedDate" required>-->
    <!--          <label>Birthdate</label>-->
    <!--        </md-datepicker>-->

    <!--        <md-field>-->
    <!--          <label>E-Mail</label>-->
    <!--          <md-input v-model="email" required></md-input>-->
    <!--          <span class="md-error">Please enter an E-Mail.</span>-->
    <!--        </md-field>-->

    <!--        <md-field>-->
    <!--          <label>Password</label>-->
    <!--          <md-input v-model="passwd" type="password" required></md-input>-->
    <!--          <span class="md-error">Please enter a Password</span>-->
    <!--        </md-field>-->

    <!--        <md-field>-->
    <!--          <label>Confirm Password</label>-->
    <!--          <md-input v-model="passwd" type="password" required></md-input>-->
    <!--          <span class="md-error">Please enter a Password.</span>-->
    <!--&lt;!&ndash;           erkennen ob leer oder nicht überein&ndash;&gt;-->
    <!--        </md-field>-->

    <!--        <md-button class="md-primary md-raised">Register</md-button>-->
    <!--      </div>&ndash;&gt;-->
    <!--    </md-card>-->
  </div>
</template>

<script>
export default {
  name: "KonradFormular",
  props: {
    title: String
  }
}
</script>

<style scoped>
#padder {
  padding: 10px;
}

.login-form {
  margin: 10px;
}
</style>
