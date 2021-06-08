<template>
    <div class="h-full flex flex-col justify-center items-center">
        <div class="w-full px-4 flex flex-col space-y-2 lg:w-96 lg:px-0">
            <form-label>Email</form-label>
            <form-input></form-input>
            <form-select></form-select>
            <form-text-area></form-text-area>
            <div class="flex justify-evenly">
                <form-radio :name="`sample`" :id="`a`" :value="`a`" @change="$event ? radio = $event.target.value : ''" :checked="true">Sample</form-radio>
                <form-radio :name="`sample`" :id="`b`" :value="`b`" @change="$event ? radio = $event.target.value : ''">Sample</form-radio>
                <form-radio :name="`sample`" :id="`c`" :value="`c`" @change="$event ? radio = $event.target.value : ''">Sample</form-radio>
            </div>
            <div class="flex justify-evenly">
                <form-checkbox :name="`sample`" :id="`d`" :value="`d`" @change="$event ? checkbox.d = $event.target.checked : ''">Sample</form-checkbox>
                <form-checkbox :name="`sample`" :id="`e`" :value="`e`" @change="$event ? checkbox.e = $event.target.checked : ''">Sample</form-checkbox>
                <form-checkbox :name="`sample`" :id="`f`" :value="`f`" @change="$event ? checkbox.f = $event.target.checked : ''">Sample</form-checkbox>
            </div>
            <button-primary>Primary</button-primary>
            <button-secondary>Secondary</button-secondary>
            <button-success>Success</button-success>
            <button-danger>Danger</button-danger>
        </div>
    </div>
</template>

<script>
    import FormInput from "./components/common/forms/FormInput";
    import FormLabel from "./components/common/forms/FormLabel";
    import FormTextArea from "./components/common/forms/FormTextArea";
    import FormSelect from "./components/common/forms/FormSelect";
    import FormSelectOption from "./components/common/forms/FormSelectOption";
    import FormRadio from "./components/common/forms/FormRadio";
    import FormCheckbox from "./components/common/forms/FormCheckbox";
    import ButtonPrimary from "./components/common/buttons/ButtonPrimary";
    import ButtonSecondary from "./components/common/buttons/ButtonSecondary";
    import ButtonDanger from "./components/common/buttons/ButtonDanger";
    import ButtonSuccess from "./components/common/buttons/ButtonSuccess";

    export default {
        name: "App",
        components: {
            ButtonSuccess,
            ButtonDanger,
            ButtonSecondary,
            ButtonPrimary,
            FormCheckbox,
            FormRadio,
            FormSelectOption,
            FormSelect,
            FormTextArea,
            FormLabel,
            FormInput,
        },
        data() {
            return {
                radio: '',
                checkbox: {
                    d: false,
                    e: false,
                    f: false,
                },
            }
        },
    }
</script>

<style scoped>

</style>
