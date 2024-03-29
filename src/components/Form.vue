<script setup lang="ts">
    const submitHandler = async (fields: any[]) => {
    await new Promise((r) => setTimeout(r, 1000))
    alert(JSON.stringify(fields))
    }
</script>

<template>
    <div class="contact-form">
        <div class="contact-form__content">
            <FormKit type="form" @submit="submitHandler" :config="{ validationVisibility: 'submit' }">
                <FormKit
                    type="text"
                    name="name"
                    id="name"
                    label="Your name"
                    placeholder="Please enter your name"
                    validation="required|text"
                    :validation-messages="{
                        required: 'Error: Please enter a valid name',
                    }"
                />

                <FormKit
                    type="tel"
                    name="phone"
                    id="phone"
                    label="Your Telephone Number"
                    placeholder="Please enter your phone number"
                    validation="required|number"
                    :validation-messages="{
                        required: 'Error: Please enter a valid phone number',
                    }"
                />

                <FormKit
                    type="email"
                    name="email"
                    id="email"
                    label="Your Email"
                    placeholder="Please enter your email"
                    validation="required|email"
                    :validation-messages="{
                        required: 'Error: Please enter a valid email',
                    }"
                />

                <FormKit
                    type="textarea"
                    name="message"
                    id="message"
                    label="Your Message"
                    help="Please enter as much detail as possible"
                    placeholder="Please enter your message"
                    validation="required|email"
                    :validation-messages="{
                        required: 'Error: This field is required',
                    }"
                />
            </FormKit>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .contact-form {

        &__content {
            form {
                padding: 0 20px;
                
                @media only screen and (min-width: 768px) {
                    max-width: 600px;
                    margin: 0 auto;
                }
            }
        }
    }
</style>

<style lang="scss">
    .formkit {

        &-wrapper {
            margin-bottom: 30px;
        }

        &-form {

            label {
                color: #0E1C2D;
                font-size: 16px;
                line-height: 30px;
            }

            input[type="text"],
            input[type="tel"],
            input[type="email"],
            textarea {
                display: block;
                width: 100%;
                padding: 8px 10px;
                border-radius: 4px;
                border: 2px solid #DADADA;
                line-height: 30px;
                outline: none;

                &:focus,
                &:focus-visible {
                    border: 2px solid #0E1C2D;
                }
            }

            .formkit-inner {
                position: relative;

                &::after {
                    content: "*";
                    position: absolute;
                    right: 24px;
                    bottom: 34px;
                    color: #D0021B;
                    width: 6px;
                    height: 6px;
                    font-size: 30px
                }
            }

            textarea {
                display: block; 
                height: 200px;
                padding: 8px 10px;
                position: relative;

                &::placeholder {
                    position: absolute;
                    bottom: 8px;
                    left: 8px;
                    text-align: left;
                    font-size: 16px;
                }
            }
        }

        &-help {
            margin: -25px 0 0 5px;
            color: #8D9CA8;
            font-size: 14px;
        }

        &-outer {
            &[data-invalid="true"] {
                input[type="text"],
                input[type="tel"],
                input[type="email"],
                textarea {
                    border-color: #D0021B;
                }

                .formkit-inner {

                }
            }
        }

        &-message {
            font-size: 14px;
            line-height: 24px;
            color: #D0021B;
            margin: -22px 0 20px;

            &:last-of-type {
                text-align: right;
            }

            &#input_0-incomplete {
                display: none;
            }
        }

        &-actions {
                text-align: center;

            @media only screen and (min-width: 768px) {
                text-align: right;
            }

            button[type="submit"] {
                background-color: #0E1C2D;
                color: #FFFFFF;
                font-size: 16px;
                border-radius: 4px;
                max-width: 280px;
                padding: 13px 121px;
                margin-top: 30px;

                @media only screen and (min-width: 768px) {
                    padding: 13px 35px;
                }
            }
        }
    }
</style>