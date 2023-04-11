# Quick Start

To quickly start processing payments in Laravel, you may use the install command, which will publish all necessary assets and generate the payment gateway skeletons & the config file so you can focus on what's important, the integration.

Once you install the package, run the `checkout:install` command and follow its instructions.

```bash
php artisan checkout:install
```

## 1. Publishing the migration.

The command will start by publishing the migration for you. This migration should have everything you need in order to start processing payments, but you may update it as you wish.

```bash
=> INFO  Publishing [migrations] assets.  

=> Copying file [vendor/payavel/checkout/src/database/migrations/2021_01_01_000000_create_base_payment_tables.php] to [database/migrations/2023_01_01_000000_create_base_payment_tables.php] DONE
```

## 2. Generating the fake payment gateway.

Then it will automatically generate the `FakePaymentRequest::class` & `FakePaymentResponse::class` files. These files allow you to leverage the `PAYMENT_TEST_MODE` for local development or testing.

```bash
=> Fake payment gateway generated successfully!
```

## 3. Generating your payment gateway(s) of choice.

Your project will prompt you to provide a payment service provider for integration.

```bash
=> What payment provider would you like to add?:
> Adyen

=> How would you like to identify the Adyen payment provider? [adyen]:
> adyen
```

Once provided, it will generate the provider's request & response classes for you.

```bash
=> Adyen payment gateway generated successfully!
```

The program will also ask if you want to include additional payment providers in your project. You can specify as many as you like, and the system will guide you through the process until you have added all the necessary providers.

```bash
=> Would you like to add another payment provider? (yes/no) [no]:
> no
```

## 4. Providing a list of merchants.
At this step, the program will prompt you to share the merchant accounts that your application will use for processing payments.

```bash
=> What payment merchant would you like to add?:
> Laravel

=> How would you like to identify the Laravel payment merchant? [laravel]:
> laravel
```
You may provide as many merchants as needed, this is very helpful when your business is segregated in different areas and you wish to keep your reporting separate.

```bash
=>  Would you like to add another payment merchant? (yes/no) [no]:
> no
```

## 5. Generating the payment configuration file.
As a final step, Payavel will generate your `payment.php` configuration file on your behalf. The foundation is ready; you just need to fill in the blanks.

```bash
=> The payment config has been successfully generated.
```
