[@bigcommerce/checkout-sdk](../README.md) › [BoltPaymentInitializeOptions](boltpaymentinitializeoptions.md)

# Interface: BoltPaymentInitializeOptions

A set of options that are required to initialize the Bolt payment method with:

1) Bolt Full Checkout:

If the customer chooses to pay with Bolt, he will be asked to
enter his payment details via Bolt Full Checkout.

```js
service.initializePayment({
    methodId: 'bolt',
});
```

2) Bolt Client:

If the customer chooses to pay with Bolt in payment section of Checkout page,
the Bolt Payment Modal will be shown, and the customer will be asked
to enter payment details via Bolt Modal

```js
service.initializePayment({
    methodId: 'bolt',
    bolt: {
        useBigCommerceCheckout: true,
    }
});
```

3) Bolt Embedded:

A set of options that are required to initialize the Bolt payment method
for presenting its credit card form.

```html
<!-- These containers are where the hosted (iframed) credit card field will be inserted -->
<div id="bolt-embedded"></div>
```

```js
service.initializePayment({
    methodId: 'bolt',
    bolt: {
        useBigCommerceCheckout: true,
        containerId: 'boltEmbeddedContainerId',
    }
});
```

## Hierarchy

* **BoltPaymentInitializeOptions**

## Index

### Properties

* [containerId](boltpaymentinitializeoptions.md#optional-containerid)
* [useBigCommerceCheckout](boltpaymentinitializeoptions.md#usebigcommercecheckout)

### Methods

* [onPaymentSelect](boltpaymentinitializeoptions.md#optional-onpaymentselect)

## Properties

### `Optional` containerId

• **containerId**? : *undefined | string*

The CSS selector of a container where the Bolt Embedded payment field should be inserted into.

___

###  useBigCommerceCheckout

• **useBigCommerceCheckout**: *boolean*

## Methods

### `Optional` onPaymentSelect

▸ **onPaymentSelect**(`hasBoltAccount`: boolean): *void*

A callback that gets called when the customer selects Bolt as payment option.

**Parameters:**

Name | Type |
------ | ------ |
`hasBoltAccount` | boolean |

**Returns:** *void*
