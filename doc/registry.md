
<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry"></a>

# Module `0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450::registry`

Market and capability registration operations.

Econia relies on a global market registry, which supports
permissionless registration of markets, as well as capabilities.
Custodian capabilities are required to approve order operations and
withdrawals, while underwriter capabilities are required to approve
generic asset amounts.

The registry is paired with a recognized market list that tabulates
a recognized market for select trading pairs. The recognized market
list can only be managed by the Econia account, and provides a set
of public APIs that allow lookup of an official market based on a
trading pair.

Custodian capabilities and underwriter capabilities are 1-indexed,
with an ID of 0 reserved as a flag for null. For consistency, market
IDs are 1-indexed too.


<a id="@General_overview_sections_0"></a>

## General overview sections


[View functions](#view-functions)

* [Constant getters](#constant-getters)
* [Market lookup](#market-lookup)

[Public function index](#public-function-index)

* [Capability management](#capability-management)
* [Integrator fee store setup](#integrator-fee-store-setup)
* [Recognized market lookup](#recognized-market-lookup)
* [Recognized market management](#recognized-market-management)

[Dependency charts](#dependency-charts)

* [Capability registration](#capability-registration)
* [Fee store registration](#fee-store-registration)
* [Market getters](#market-getters)
* [Recognized market setters](#recognized-market-setters)
* [Internal market registration](#internal-market-registration)

[Complete DocGen index](#complete-docgen-index)


<a id="@View_functions_1"></a>

## View functions



<a id="@Constant_getters_2"></a>

### Constant getters


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_MAX_CHARACTERS_GENERIC">get_MAX_CHARACTERS_GENERIC</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_MIN_CHARACTERS_GENERIC">get_MIN_CHARACTERS_GENERIC</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_NO_CUSTODIAN">get_NO_CUSTODIAN</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_NO_UNDERWRITER">get_NO_UNDERWRITER</a>()</code>


<a id="@Market_lookup_3"></a>

### Market lookup


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_market_counts">get_market_counts</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_market_info">get_market_info</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_market_id_base_coin">get_market_id_base_coin</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_market_id_base_generic">get_market_id_base_generic</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_id_base_coin">get_recognized_market_id_base_coin</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_id_base_generic">get_recognized_market_id_base_generic</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_coin_by_type">has_recognized_market_base_coin_by_type</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_generic_by_type">has_recognized_market_base_generic_by_type</a>()</code>


<a id="@Public_function_index_4"></a>

## Public function index



<a id="@Capability_management_5"></a>

### Capability management


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_custodian_id">get_custodian_id</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_underwriter_id">get_underwriter_id</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_custodian_capability">register_custodian_capability</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_underwriter_capability">register_underwriter_capability</a>()</code>


<a id="@Integrator_fee_store_setup_6"></a>

### Integrator fee store setup


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store">register_integrator_fee_store</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store_base_tier">register_integrator_fee_store_base_tier</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store_from_coinstore">register_integrator_fee_store_from_coinstore</a>()</code>


<a id="@Recognized_market_lookup_7"></a>

### Recognized market lookup


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_coin">get_recognized_market_info_base_coin</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_coin_by_type">get_recognized_market_info_base_coin_by_type</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_generic">get_recognized_market_info_base_generic</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_generic_by_type">get_recognized_market_info_base_generic_by_type</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_coin">has_recognized_market_base_coin</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_generic">has_recognized_market_base_generic</a>()</code>


<a id="@Recognized_market_management_8"></a>

### Recognized market management


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_remove_recognized_market">remove_recognized_market</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_remove_recognized_markets">remove_recognized_markets</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_set_recognized_market">set_recognized_market</a>()</code>
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_set_recognized_markets">set_recognized_markets</a>()</code>

(These are public entry functions.)


<a id="@Dependency_charts_9"></a>

## Dependency charts


The below dependency charts use <code>mermaid.js</code> syntax, which can be
automatically rendered into a diagram (depending on the browser)
when viewing the documentation file generated from source code. If
a browser renders the diagrams with coloring that makes it difficult
to read, try a different browser.


<a id="@Capability_registration_10"></a>

### Capability registration


```mermaid

flowchart LR

register_custodian_capability -->
incentives::deposit_custodian_registration_utility_coins
register_underwriter_capability -->
incentives::deposit_underwriter_registration_utility_coins

```


<a id="@Fee_store_registration_11"></a>

### Fee store registration


```mermaid

flowchart LR

register_integrator_fee_store_base_tier -->
register_integrator_fee_store
register_integrator_fee_store_from_coinstore -->
register_integrator_fee_store

```


<a id="@Market_getters_12"></a>

### Market getters


```mermaid

flowchart LR

get_recognized_market_info_base_coin -->
get_recognized_market_info
get_recognized_market_info_base_coin_by_type -->
get_recognized_market_info_base_coin
get_recognized_market_info_base_generic -->
get_recognized_market_info
get_recognized_market_info_base_generic_by_type  -->
get_recognized_market_info_base_generic

has_recognized_market_base_coin --> has_recognized_market
has_recognized_market_base_coin_by_type -->
has_recognized_market_base_coin
has_recognized_market_base_generic --> has_recognized_market
has_recognized_market_base_generic_by_type -->
has_recognized_market_base_generic

get_recognized_market_id_base_coin -->
get_recognized_market_info_base_coin_by_type

get_recognized_market_id_base_generic -->
get_recognized_market_info_base_generic_by_type

get_market_info --> has_recognized_market
get_market_info --> get_recognized_market_info

get_market_id_base_coin --> get_market_id
get_market_id_base_generic --> get_market_id

```


<a id="@Recognized_market_setters_13"></a>

### Recognized market setters


```mermaid

flowchart LR

remove_recognized_markets --> remove_recognized_market
set_recognized_markets --> set_recognized_market

```


<a id="@Internal_market_registration_14"></a>

### Internal market registration


```mermaid

flowchart LR

register_market_base_coin_internal --> register_market_internal
register_market_base_generic_internal --> register_market_internal

register_market_internal -->
incentives::deposit_market_registration_utility_coins

```


<a id="@Complete_DocGen_index_15"></a>

## Complete DocGen index


The below index is automatically generated from source code:


-  [General overview sections](#@General_overview_sections_0)
-  [View functions](#@View_functions_1)
    -  [Constant getters](#@Constant_getters_2)
    -  [Market lookup](#@Market_lookup_3)
-  [Public function index](#@Public_function_index_4)
    -  [Capability management](#@Capability_management_5)
    -  [Integrator fee store setup](#@Integrator_fee_store_setup_6)
    -  [Recognized market lookup](#@Recognized_market_lookup_7)
    -  [Recognized market management](#@Recognized_market_management_8)
-  [Dependency charts](#@Dependency_charts_9)
    -  [Capability registration](#@Capability_registration_10)
    -  [Fee store registration](#@Fee_store_registration_11)
    -  [Market getters](#@Market_getters_12)
    -  [Recognized market setters](#@Recognized_market_setters_13)
    -  [Internal market registration](#@Internal_market_registration_14)
-  [Complete DocGen index](#@Complete_DocGen_index_15)
-  [Struct `AssetTypeView`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_AssetTypeView)
-  [Struct `CustodianCapability`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_CustodianCapability)
-  [Resource `GenericAsset`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_GenericAsset)
-  [Struct `MarketCounts`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketCounts)
-  [Struct `MarketInfo`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketInfo)
-  [Struct `MarketInfoView`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketInfoView)
-  [Struct `MarketRegistrationEvent`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketRegistrationEvent)
-  [Struct `RecognizedMarketEvent`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_RecognizedMarketEvent)
-  [Struct `RecognizedMarketInfo`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_RecognizedMarketInfo)
-  [Resource `RecognizedMarkets`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_RecognizedMarkets)
-  [Resource `Registry`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_Registry)
-  [Struct `TradingPair`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_TradingPair)
-  [Struct `UnderwriterCapability`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_UnderwriterCapability)
-  [Constants](#@Constants_16)
-  [Function `get_MAX_CHARACTERS_GENERIC`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_MAX_CHARACTERS_GENERIC)
    -  [Testing](#@Testing_17)
-  [Function `get_MIN_CHARACTERS_GENERIC`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_MIN_CHARACTERS_GENERIC)
    -  [Testing](#@Testing_18)
-  [Function `get_NO_CUSTODIAN`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_NO_CUSTODIAN)
    -  [Testing](#@Testing_19)
-  [Function `get_NO_UNDERWRITER`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_NO_UNDERWRITER)
    -  [Testing](#@Testing_20)
-  [Function `get_recognized_market_id_base_coin`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_id_base_coin)
    -  [Testing](#@Testing_21)
-  [Function `get_recognized_market_id_base_generic`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_id_base_generic)
    -  [Testing](#@Testing_22)
-  [Function `has_recognized_market_base_coin_by_type`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_coin_by_type)
    -  [Type parameters](#@Type_parameters_23)
    -  [Testing](#@Testing_24)
-  [Function `has_recognized_market_base_generic_by_type`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_generic_by_type)
    -  [Type parameters](#@Type_parameters_25)
    -  [Parameters](#@Parameters_26)
    -  [Testing](#@Testing_27)
-  [Function `get_custodian_id`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_custodian_id)
    -  [Testing](#@Testing_28)
-  [Function `get_recognized_market_info_base_coin`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_coin)
    -  [Parameters](#@Parameters_29)
    -  [Testing](#@Testing_30)
-  [Function `get_recognized_market_info_base_coin_by_type`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_coin_by_type)
    -  [Type parameters](#@Type_parameters_31)
    -  [Testing](#@Testing_32)
-  [Function `get_recognized_market_info_base_generic`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_generic)
    -  [Parameters](#@Parameters_33)
    -  [Testing](#@Testing_34)
-  [Function `get_recognized_market_info_base_generic_by_type`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_generic_by_type)
    -  [Type parameters](#@Type_parameters_35)
    -  [Parameters](#@Parameters_36)
    -  [Testing](#@Testing_37)
-  [Function `get_underwriter_id`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_underwriter_id)
    -  [Testing](#@Testing_38)
-  [Function `has_recognized_market_base_coin`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_coin)
    -  [Parameters](#@Parameters_39)
    -  [Testing](#@Testing_40)
-  [Function `has_recognized_market_base_generic`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_generic)
    -  [Parameters](#@Parameters_41)
    -  [Testing](#@Testing_42)
-  [Function `register_custodian_capability`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_custodian_capability)
    -  [Testing](#@Testing_43)
-  [Function `register_integrator_fee_store`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store)
    -  [Type parameters](#@Type_parameters_44)
    -  [Parameters](#@Parameters_45)
    -  [Aborts](#@Aborts_46)
    -  [Testing](#@Testing_47)
-  [Function `register_underwriter_capability`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_underwriter_capability)
    -  [Testing](#@Testing_48)
-  [Function `register_integrator_fee_store_base_tier`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store_base_tier)
    -  [Testing](#@Testing_49)
-  [Function `register_integrator_fee_store_from_coinstore`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store_from_coinstore)
    -  [Testing](#@Testing_50)
-  [Function `remove_recognized_market`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_remove_recognized_market)
    -  [Parameters](#@Parameters_51)
    -  [Emits](#@Emits_52)
    -  [Aborts](#@Aborts_53)
    -  [Assumptions](#@Assumptions_54)
    -  [Testing](#@Testing_55)
-  [Function `remove_recognized_markets`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_remove_recognized_markets)
    -  [Testing](#@Testing_56)
-  [Function `set_recognized_market`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_set_recognized_market)
    -  [Parameters](#@Parameters_57)
    -  [Emits](#@Emits_58)
    -  [Aborts](#@Aborts_59)
    -  [Assumptions](#@Assumptions_60)
    -  [Testing](#@Testing_61)
-  [Function `set_recognized_markets`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_set_recognized_markets)
    -  [Testing](#@Testing_62)
-  [Function `get_market_info_for_market_account`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_market_info_for_market_account)
    -  [Parameters](#@Parameters_63)
    -  [Returns](#@Returns_64)
    -  [Aborts](#@Aborts_65)
    -  [Testing](#@Testing_66)
-  [Function `is_registered_custodian_id`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_is_registered_custodian_id)
    -  [Testing](#@Testing_67)
-  [Function `register_market_base_coin_internal`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_market_base_coin_internal)
    -  [Aborts](#@Aborts_68)
    -  [Testing](#@Testing_69)
-  [Function `register_market_base_generic_internal`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_market_base_generic_internal)
    -  [Aborts](#@Aborts_70)
    -  [Testing](#@Testing_71)


<pre><code><b>use</b> <a href="">0x1::coin</a>;
<b>use</b> <a href="">0x1::event</a>;
<b>use</b> <a href="">0x1::option</a>;
<b>use</b> <a href="">0x1::signer</a>;
<b>use</b> <a href="">0x1::string</a>;
<b>use</b> <a href="">0x1::table</a>;
<b>use</b> <a href="">0x1::type_info</a>;
<b>use</b> <a href="incentives.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_incentives">0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450::incentives</a>;
<b>use</b> <a href="tablist.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_tablist">0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450::tablist</a>;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_AssetTypeView"></a>

## Struct `AssetTypeView`

Human-readable asset type descriptor for view functions.


<pre><code><b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_AssetTypeView">AssetTypeView</a> <b>has</b> <b>copy</b>, drop
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_CustodianCapability"></a>

## Struct `CustodianCapability`

Custodian capability required to approve order operations and
withdrawals. Administered to third-party registrants who may
store it as they wish.


<pre><code><b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_CustodianCapability">CustodianCapability</a> <b>has</b> store
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_GenericAsset"></a>

## Resource `GenericAsset`

Type flag for generic asset. Must be passed as base asset type
argument for generic market operations. Has key ability to
restrict unexpected malicious attack vectors.


<pre><code><b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_GenericAsset">GenericAsset</a> <b>has</b> key
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketCounts"></a>

## Struct `MarketCounts`

View function return specifying number of markets and recognized
markets that have been registered.


<pre><code><b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketCounts">MarketCounts</a> <b>has</b> <b>copy</b>, drop
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketInfo"></a>

## Struct `MarketInfo`

Information about a market.


<pre><code><b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketInfo">MarketInfo</a> <b>has</b> <b>copy</b>, drop, store
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketInfoView"></a>

## Struct `MarketInfoView`

Human-readable market info return for view functions.


<pre><code><b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketInfoView">MarketInfoView</a> <b>has</b> <b>copy</b>, drop
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketRegistrationEvent"></a>

## Struct `MarketRegistrationEvent`

Emitted when a market is registered.


<pre><code>#[<a href="">event</a>]
<b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketRegistrationEvent">MarketRegistrationEvent</a> <b>has</b> drop, store
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_RecognizedMarketEvent"></a>

## Struct `RecognizedMarketEvent`

Emitted when a recognized market is added, removed, or updated.


<pre><code>#[<a href="">event</a>]
<b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_RecognizedMarketEvent">RecognizedMarketEvent</a> <b>has</b> drop, store
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_RecognizedMarketInfo"></a>

## Struct `RecognizedMarketInfo`

Recognized market info for a given trading pair.


<pre><code><b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_RecognizedMarketInfo">RecognizedMarketInfo</a> <b>has</b> <b>copy</b>, drop, store
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_RecognizedMarkets"></a>

## Resource `RecognizedMarkets`

Recognized markets for specific trading pairs.


<pre><code><b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_RecognizedMarkets">RecognizedMarkets</a> <b>has</b> key
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_Registry"></a>

## Resource `Registry`

Global registration information.


<pre><code><b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_Registry">Registry</a> <b>has</b> key
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_TradingPair"></a>

## Struct `TradingPair`

A combination of a base asset and a quote asset.


<pre><code><b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_TradingPair">TradingPair</a> <b>has</b> <b>copy</b>, drop, store
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_UnderwriterCapability"></a>

## Struct `UnderwriterCapability`

Underwriter capability required to verify generic asset
amounts. Administered to third-party registrants who may store
it as they wish.


<pre><code><b>struct</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_UnderwriterCapability">UnderwriterCapability</a> <b>has</b> store
</code></pre>



<a id="@Constants_16"></a>

## Constants


<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_NOT_ECONIA"></a>

Caller is not Econia, but should be.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_NOT_ECONIA">E_NOT_ECONIA</a>: u64 = 9;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_BASE_NOT_COIN"></a>

Base coin type has not been initialized for a pure coin market.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_BASE_NOT_COIN">E_BASE_NOT_COIN</a>: u64 = 6;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_BASE_QUOTE_SAME"></a>

Base and quote asset descriptors are identical.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_BASE_QUOTE_SAME">E_BASE_QUOTE_SAME</a>: u64 = 4;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_GENERIC_TOO_FEW_CHARACTERS"></a>

Generic base asset descriptor has too few characters.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_GENERIC_TOO_FEW_CHARACTERS">E_GENERIC_TOO_FEW_CHARACTERS</a>: u64 = 7;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_GENERIC_TOO_MANY_CHARACTERS"></a>

Generic base asset descriptor has too many characters.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_GENERIC_TOO_MANY_CHARACTERS">E_GENERIC_TOO_MANY_CHARACTERS</a>: u64 = 8;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_INVALID_BASE"></a>

Base asset type is invalid.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_INVALID_BASE">E_INVALID_BASE</a>: u64 = 13;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_INVALID_MARKET_ID"></a>

Market ID is invalid.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_INVALID_MARKET_ID">E_INVALID_MARKET_ID</a>: u64 = 12;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_INVALID_QUOTE"></a>

Quote asset type is invalid.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_INVALID_QUOTE">E_INVALID_QUOTE</a>: u64 = 14;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_LOT_SIZE_0"></a>

Lot size specified as 0.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_LOT_SIZE_0">E_LOT_SIZE_0</a>: u64 = 0;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_MARKET_REGISTERED"></a>

Market is already registered.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_MARKET_REGISTERED">E_MARKET_REGISTERED</a>: u64 = 5;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_MIN_SIZE_0"></a>

Minimum order size specified as 0.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_MIN_SIZE_0">E_MIN_SIZE_0</a>: u64 = 2;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_NO_RECOGNIZED_MARKET"></a>

Trading pair does not have recognized market.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_NO_RECOGNIZED_MARKET">E_NO_RECOGNIZED_MARKET</a>: u64 = 10;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_QUOTE_NOT_COIN"></a>

Quote asset type has not been initialized as a coin.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_QUOTE_NOT_COIN">E_QUOTE_NOT_COIN</a>: u64 = 3;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_TICK_SIZE_0"></a>

Tick size specified as 0.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_TICK_SIZE_0">E_TICK_SIZE_0</a>: u64 = 1;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_WRONG_RECOGNIZED_MARKET"></a>

Market ID is not recognized for corresponding trading pair.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_WRONG_RECOGNIZED_MARKET">E_WRONG_RECOGNIZED_MARKET</a>: u64 = 11;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MAX_CHARACTERS_GENERIC"></a>

Maximum number of characters permitted in a generic asset name,
equal to the maximum number of characters permitted in a comment
line per PEP 8.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MAX_CHARACTERS_GENERIC">MAX_CHARACTERS_GENERIC</a>: u64 = 72;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MIN_CHARACTERS_GENERIC"></a>

Minimum number of characters permitted in a generic asset name,
equal to the number of spaces in an indentation level per PEP 8.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MIN_CHARACTERS_GENERIC">MIN_CHARACTERS_GENERIC</a>: u64 = 4;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_NO_CUSTODIAN"></a>

Custodian ID flag for no custodian.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_NO_CUSTODIAN">NO_CUSTODIAN</a>: u64 = 0;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_NO_UNDERWRITER"></a>

Underwriter ID flag for no underwriter.


<pre><code><b>const</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_NO_UNDERWRITER">NO_UNDERWRITER</a>: u64 = 0;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_MAX_CHARACTERS_GENERIC"></a>

## Function `get_MAX_CHARACTERS_GENERIC`

Public constant getter for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MAX_CHARACTERS_GENERIC">MAX_CHARACTERS_GENERIC</a></code>.


<a id="@Testing_17"></a>

### Testing


* <code>test_get_MAX_CHARACTERS_GENERIC()</code>


<pre><code>#[view]
<b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_MAX_CHARACTERS_GENERIC">get_MAX_CHARACTERS_GENERIC</a>(): u64
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_MIN_CHARACTERS_GENERIC"></a>

## Function `get_MIN_CHARACTERS_GENERIC`

Public constant getter for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MIN_CHARACTERS_GENERIC">MIN_CHARACTERS_GENERIC</a></code>.


<a id="@Testing_18"></a>

### Testing


* <code>test_get_MIN_CHARACTERS_GENERIC()</code>


<pre><code>#[view]
<b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_MIN_CHARACTERS_GENERIC">get_MIN_CHARACTERS_GENERIC</a>(): u64
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_NO_CUSTODIAN"></a>

## Function `get_NO_CUSTODIAN`

Public constant getter for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_NO_CUSTODIAN">NO_CUSTODIAN</a></code>.


<a id="@Testing_19"></a>

### Testing


* <code>test_get_NO_CUSTODIAN()</code>


<pre><code>#[view]
<b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_NO_CUSTODIAN">get_NO_CUSTODIAN</a>(): u64
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_NO_UNDERWRITER"></a>

## Function `get_NO_UNDERWRITER`

Public constant getter for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_NO_UNDERWRITER">NO_UNDERWRITER</a></code>.


<a id="@Testing_20"></a>

### Testing


* <code>test_get_NO_UNDERWRITER()</code>


<pre><code>#[view]
<b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_NO_UNDERWRITER">get_NO_UNDERWRITER</a>(): u64
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_id_base_coin"></a>

## Function `get_recognized_market_id_base_coin`

Return recognized market ID for a pure coin trading pair.


<a id="@Testing_21"></a>

### Testing


* <code>test_set_remove_check_recognized_markets()</code>


<pre><code>#[view]
<b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_id_base_coin">get_recognized_market_id_base_coin</a>&lt;BaseCoinType, QuoteCoinType&gt;(): u64
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_id_base_generic"></a>

## Function `get_recognized_market_id_base_generic`

Return recognized market ID for trading pair with generic base
asset.


<a id="@Testing_22"></a>

### Testing


* <code>test_set_remove_check_recognized_markets()</code>


<pre><code>#[view]
<b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_id_base_generic">get_recognized_market_id_base_generic</a>&lt;QuoteCoinType&gt;(base_name_generic: <a href="_String">string::String</a>): u64
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_coin_by_type"></a>

## Function `has_recognized_market_base_coin_by_type`

Wrapper for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_coin">has_recognized_market_base_coin</a>()</code> with type
parameters.


<a id="@Type_parameters_23"></a>

### Type parameters


* <code>BaseCoinType</code>: Base asset phantom coin type.
* <code>QuoteCoinType</code>: Quote asset phantom coin type.


<a id="@Testing_24"></a>

### Testing


* <code>test_set_remove_check_recognized_markets()</code>


<pre><code>#[view]
<b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_coin_by_type">has_recognized_market_base_coin_by_type</a>&lt;BaseCoinType, QuoteCoinType&gt;(): bool
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_generic_by_type"></a>

## Function `has_recognized_market_base_generic_by_type`

Wrapper for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_generic">has_recognized_market_base_generic</a>()</code> with quote
type parameter.


<a id="@Type_parameters_25"></a>

### Type parameters


* <code>QuoteCoinType</code>: Quote asset phantom coin type.


<a id="@Parameters_26"></a>

### Parameters


* <code>base_name_generic</code>: Generic base asset name.


<a id="@Testing_27"></a>

### Testing


* <code>test_set_remove_check_recognized_markets()</code>


<pre><code>#[view]
<b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_generic_by_type">has_recognized_market_base_generic_by_type</a>&lt;QuoteCoinType&gt;(base_name_generic: <a href="_String">string::String</a>): bool
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_custodian_id"></a>

## Function `get_custodian_id`

Return serial ID of given <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_CustodianCapability">CustodianCapability</a></code>.


<a id="@Testing_28"></a>

### Testing


* <code>test_register_capabilities()</code>


<pre><code><b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_custodian_id">get_custodian_id</a>(custodian_capability_ref: &<a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_CustodianCapability">registry::CustodianCapability</a>): u64
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_coin"></a>

## Function `get_recognized_market_info_base_coin`

Wrapper for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info">get_recognized_market_info</a>()</code> for coin base asset.


<a id="@Parameters_29"></a>

### Parameters


* <code>base_type</code>: Base asset phantom coin type info.
* <code>quote_type</code>: Quote asset phantom coin type info.


<a id="@Testing_30"></a>

### Testing


* <code>test_set_remove_check_recognized_markets()</code>


<pre><code><b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_coin">get_recognized_market_info_base_coin</a>(base_type: <a href="_TypeInfo">type_info::TypeInfo</a>, quote_type: <a href="_TypeInfo">type_info::TypeInfo</a>): (u64, u64, u64, u64, u64)
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_coin_by_type"></a>

## Function `get_recognized_market_info_base_coin_by_type`

Wrapper for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_coin">get_recognized_market_info_base_coin</a>()</code> with
type parameters.


<a id="@Type_parameters_31"></a>

### Type parameters


* <code>BaseCoinType</code>: Base asset phantom coin type.
* <code>QuoteCoinType</code>: Quote asset phantom coin type.


<a id="@Testing_32"></a>

### Testing


* <code>test_set_remove_check_recognized_markets()</code>


<pre><code><b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_coin_by_type">get_recognized_market_info_base_coin_by_type</a>&lt;BaseCoinType, QuoteCoinType&gt;(): (u64, u64, u64, u64, u64)
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_generic"></a>

## Function `get_recognized_market_info_base_generic`

Wrapper for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info">get_recognized_market_info</a>()</code> for generic base
asset.


<a id="@Parameters_33"></a>

### Parameters


* <code>base_name_generic</code>: Generic base asset name.
* <code>quote_type</code>: Quote asset phantom coin type info.


<a id="@Testing_34"></a>

### Testing


* <code>test_set_remove_check_recognized_markets()</code>


<pre><code><b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_generic">get_recognized_market_info_base_generic</a>(base_name_generic: <a href="_String">string::String</a>, quote_type: <a href="_TypeInfo">type_info::TypeInfo</a>): (u64, u64, u64, u64, u64)
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_generic_by_type"></a>

## Function `get_recognized_market_info_base_generic_by_type`

Wrapper for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_generic">get_recognized_market_info_base_generic</a>()</code> with
quote type parameter.


<a id="@Type_parameters_35"></a>

### Type parameters


* <code>QuoteCoinType</code>: Quote asset phantom coin type.


<a id="@Parameters_36"></a>

### Parameters


* <code>base_name_generic</code>: Generic base asset name.


<a id="@Testing_37"></a>

### Testing


* <code>test_set_remove_check_recognized_markets()</code>


<pre><code><b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_recognized_market_info_base_generic_by_type">get_recognized_market_info_base_generic_by_type</a>&lt;QuoteCoinType&gt;(base_name_generic: <a href="_String">string::String</a>): (u64, u64, u64, u64, u64)
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_underwriter_id"></a>

## Function `get_underwriter_id`

Return serial ID of given <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_UnderwriterCapability">UnderwriterCapability</a></code>.


<a id="@Testing_38"></a>

### Testing


* <code>test_register_capabilities()</code>


<pre><code><b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_underwriter_id">get_underwriter_id</a>(underwriter_capability_ref: &<a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_UnderwriterCapability">registry::UnderwriterCapability</a>): u64
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_coin"></a>

## Function `has_recognized_market_base_coin`

Wrapper for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market">has_recognized_market</a>()</code> for coin base asset.


<a id="@Parameters_39"></a>

### Parameters


* <code>base_type</code>: Base asset phantom coin type info.
* <code>quote_type</code>: Quote asset phantom coin type info.


<a id="@Testing_40"></a>

### Testing


* <code>test_set_remove_check_recognized_markets()</code>


<pre><code><b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_coin">has_recognized_market_base_coin</a>(base_type: <a href="_TypeInfo">type_info::TypeInfo</a>, quote_type: <a href="_TypeInfo">type_info::TypeInfo</a>): bool
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_generic"></a>

## Function `has_recognized_market_base_generic`

Wrapper for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market">has_recognized_market</a>()</code> for generic base asset.


<a id="@Parameters_41"></a>

### Parameters


* <code>base_name_generic</code>: Generic base asset name.
* <code>quote_type</code>: Quote asset phantom coin type info.


<a id="@Testing_42"></a>

### Testing


* <code>test_set_remove_check_recognized_markets()</code>


<pre><code><b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_has_recognized_market_base_generic">has_recognized_market_base_generic</a>(base_name_generic: <a href="_String">string::String</a>, quote_type: <a href="_TypeInfo">type_info::TypeInfo</a>): bool
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_custodian_capability"></a>

## Function `register_custodian_capability`

Return a unique <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_CustodianCapability">CustodianCapability</a></code>.

Increment the number of registered custodians, then issue a
capability with the corresponding serial ID. Requires utility
coins to cover the custodian registration fee.


<a id="@Testing_43"></a>

### Testing


* <code>test_register_capabilities()</code>


<pre><code><b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_custodian_capability">register_custodian_capability</a>&lt;UtilityCoinType&gt;(utility_coins: <a href="_Coin">coin::Coin</a>&lt;UtilityCoinType&gt;): <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_CustodianCapability">registry::CustodianCapability</a>
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store"></a>

## Function `register_integrator_fee_store`

Register integrator fee store to given tier on given market.


<a id="@Type_parameters_44"></a>

### Type parameters


* <code>QuoteCoinType</code>: The quote coin type for market.
* <code>UtilityCoinType</code>: The utility coin type.


<a id="@Parameters_45"></a>

### Parameters


* <code>integrator</code>: Integrator account.
* <code>market_id</code>: Market ID for corresponding market.
* <code>tier</code>: <code><a href="incentives.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_incentives_IntegratorFeeStore">incentives::IntegratorFeeStore</a></code> tier to activate to.
* <code>utility_coins</code>: Utility coins paid to activate to given tier.


<a id="@Aborts_46"></a>

### Aborts


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_INVALID_MARKET_ID">E_INVALID_MARKET_ID</a></code>: No such registered market ID.
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_INVALID_QUOTE">E_INVALID_QUOTE</a></code>: Invalid quote coin type for market.


<a id="@Testing_47"></a>

### Testing


* <code>test_register_integrator_fee_store_invalid_market_id()</code>
* <code>test_register_integrator_fee_store_invalid_quote()</code>
* <code>test_register_integrator_fee_stores()</code>


<pre><code><b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store">register_integrator_fee_store</a>&lt;QuoteCoinType, UtilityCoinType&gt;(integrator: &<a href="">signer</a>, market_id: u64, tier: u8, utility_coins: <a href="_Coin">coin::Coin</a>&lt;UtilityCoinType&gt;)
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_underwriter_capability"></a>

## Function `register_underwriter_capability`

Return a unique <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_UnderwriterCapability">UnderwriterCapability</a></code>.

Increment the number of registered underwriters, then issue a
capability with the corresponding serial ID. Requires utility
coins to cover the underwriter registration fee.


<a id="@Testing_48"></a>

### Testing


* <code>test_register_capabilities()</code>


<pre><code><b>public</b> <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_underwriter_capability">register_underwriter_capability</a>&lt;UtilityCoinType&gt;(utility_coins: <a href="_Coin">coin::Coin</a>&lt;UtilityCoinType&gt;): <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_UnderwriterCapability">registry::UnderwriterCapability</a>
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store_base_tier"></a>

## Function `register_integrator_fee_store_base_tier`

Wrapped call to <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store">register_integrator_fee_store</a>()</code> for activating
to base tier, which does not require utility coins.


<a id="@Testing_49"></a>

### Testing


* <code>test_register_integrator_fee_stores()</code>


<pre><code><b>public</b> entry <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store_base_tier">register_integrator_fee_store_base_tier</a>&lt;QuoteCoinType, UtilityCoinType&gt;(integrator: &<a href="">signer</a>, market_id: u64)
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store_from_coinstore"></a>

## Function `register_integrator_fee_store_from_coinstore`

Wrapped call to <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store">register_integrator_fee_store</a>()</code> for paying
utility coins from an <code>supra_framework::coin::CoinStore</code>.


<a id="@Testing_50"></a>

### Testing


* <code>test_register_integrator_fee_stores()</code>


<pre><code><b>public</b> entry <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_integrator_fee_store_from_coinstore">register_integrator_fee_store_from_coinstore</a>&lt;QuoteCoinType, UtilityCoinType&gt;(integrator: &<a href="">signer</a>, market_id: u64, tier: u8)
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_remove_recognized_market"></a>

## Function `remove_recognized_market`

Remove market having given ID from recognized markets list.


<a id="@Parameters_51"></a>

### Parameters


* <code><a href="">account</a></code>: Econia account.
* <code>market_id</code>: Market ID to recognize.


<a id="@Emits_52"></a>

### Emits


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_RecognizedMarketEvent">RecognizedMarketEvent</a></code>: Info about recognized market for
given trading pair.


<a id="@Aborts_53"></a>

### Aborts


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_NOT_ECONIA">E_NOT_ECONIA</a></code>: <code><a href="">account</a></code> is not Econia.
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_NO_RECOGNIZED_MARKET">E_NO_RECOGNIZED_MARKET</a></code>: Market having given ID is not a
recognized market.
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_WRONG_RECOGNIZED_MARKET">E_WRONG_RECOGNIZED_MARKET</a></code>: Market ID is not recognized for
corresponding trading pair.


<a id="@Assumptions_54"></a>

### Assumptions


* <code>market_id</code> corresponds to a registered market.


<a id="@Testing_55"></a>

### Testing


* <code>test_remove_recognized_market_no_recognized()</code>
* <code>test_remove_recognized_market_not_econia()</code>
* <code>test_remove_recognized_market_wrong_market()</code>
* <code>test_set_remove_check_recognized_markets()</code>


<pre><code><b>public</b> entry <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_remove_recognized_market">remove_recognized_market</a>(<a href="">account</a>: &<a href="">signer</a>, market_id: u64)
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_remove_recognized_markets"></a>

## Function `remove_recognized_markets`

Wrapper for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_remove_recognized_market">remove_recognized_market</a>()</code> with market IDs vector.


<a id="@Testing_56"></a>

### Testing


* <code>test_set_remove_check_recognized_markets()</code>


<pre><code><b>public</b> entry <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_remove_recognized_markets">remove_recognized_markets</a>(<a href="">account</a>: &<a href="">signer</a>, market_ids: <a href="">vector</a>&lt;u64&gt;)
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_set_recognized_market"></a>

## Function `set_recognized_market`

Set market having given ID as recognized market.


<a id="@Parameters_57"></a>

### Parameters


* <code><a href="">account</a></code>: Econia account.
* <code>market_id</code>: Market ID to recognize.


<a id="@Emits_58"></a>

### Emits


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_RecognizedMarketEvent">RecognizedMarketEvent</a></code>: Info about recognized market for
given trading pair.


<a id="@Aborts_59"></a>

### Aborts


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_NOT_ECONIA">E_NOT_ECONIA</a></code>: <code><a href="">account</a></code> is not Econia.


<a id="@Assumptions_60"></a>

### Assumptions


* <code>market_id</code> corresponds to a registered market.


<a id="@Testing_61"></a>

### Testing


* <code>test_set_recognized_market_not_econia()</code>
* <code>test_set_recognized_market_update()</code>
* <code>test_set_remove_check_recognized_markets()</code>


<pre><code><b>public</b> entry <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_set_recognized_market">set_recognized_market</a>(<a href="">account</a>: &<a href="">signer</a>, market_id: u64)
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_set_recognized_markets"></a>

## Function `set_recognized_markets`

Wrapper for <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_set_recognized_market">set_recognized_market</a>()</code> with market IDs vector.


<a id="@Testing_62"></a>

### Testing


* <code>test_set_remove_check_recognized_markets()</code>


<pre><code><b>public</b> entry <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_set_recognized_markets">set_recognized_markets</a>(<a href="">account</a>: &<a href="">signer</a>, market_ids: <a href="">vector</a>&lt;u64&gt;)
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_market_info_for_market_account"></a>

## Function `get_market_info_for_market_account`

Check types, return market info for market account registration.

Restricted to friends to prevent excessive public queries
against the registry.


<a id="@Parameters_63"></a>

### Parameters


* <code>market_id</code>: Market ID to check.
* <code>base_type</code>: Base type to check.
* <code>quote_type</code>: Quote type to check.


<a id="@Returns_64"></a>

### Returns


* <code>String</code>: <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketInfo">MarketInfo</a>.base_name_generic</code>.
* <code>u64</code>: <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketInfo">MarketInfo</a>.lot_size</code>.
* <code>u64</code>: <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketInfo">MarketInfo</a>.tick_size</code>.
* <code>u64</code>: <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketInfo">MarketInfo</a>.min_size</code>.
* <code>u64</code>: <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_MarketInfo">MarketInfo</a>.underwriter_id</code>.


<a id="@Aborts_65"></a>

### Aborts


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_INVALID_MARKET_ID">E_INVALID_MARKET_ID</a></code>: Market ID is invalid.
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_INVALID_BASE">E_INVALID_BASE</a></code>: Base asset type is invalid.
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_INVALID_QUOTE">E_INVALID_QUOTE</a></code>: Quote asset type is invalid.


<a id="@Testing_66"></a>

### Testing


* <code>test_get_market_info_for_market_account()</code>
* <code>test_get_market_info_for_market_account_invalid_base()</code>
* <code>test_get_market_info_for_market_account_invalid_market_id()</code>
* <code>test_get_market_info_for_market_account_invalid_quote()</code>


<pre><code><b>public</b>(<b>friend</b>) <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_get_market_info_for_market_account">get_market_info_for_market_account</a>(market_id: u64, base_type: <a href="_TypeInfo">type_info::TypeInfo</a>, quote_type: <a href="_TypeInfo">type_info::TypeInfo</a>): (<a href="_String">string::String</a>, u64, u64, u64, u64)
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_is_registered_custodian_id"></a>

## Function `is_registered_custodian_id`

Return <code><b>true</b></code> if <code>custodian_id</code> has been registered.

Restricted to friends to prevent excessive public queries
against the registry.


<a id="@Testing_67"></a>

### Testing


* <code>test_register_capabilities()</code>


<pre><code><b>public</b>(<b>friend</b>) <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_is_registered_custodian_id">is_registered_custodian_id</a>(custodian_id: u64): bool
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_market_base_coin_internal"></a>

## Function `register_market_base_coin_internal`

Wrapped market registration call for a base coin type.

See inner function <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_market_internal">register_market_internal</a>()</code>.


<a id="@Aborts_68"></a>

### Aborts


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_BASE_NOT_COIN">E_BASE_NOT_COIN</a></code>: Base coin type is not initialized.


<a id="@Testing_69"></a>

### Testing


* <code>test_register_market_base_not_coin()</code>
* <code>test_register_market_base_coin_internal()</code>


<pre><code><b>public</b>(<b>friend</b>) <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_market_base_coin_internal">register_market_base_coin_internal</a>&lt;BaseCoinType, QuoteCoinType, UtilityCoinType&gt;(lot_size: u64, tick_size: u64, min_size: u64, utility_coins: <a href="_Coin">coin::Coin</a>&lt;UtilityCoinType&gt;): u64
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_market_base_generic_internal"></a>

## Function `register_market_base_generic_internal`

Wrapped market registration call for a generic base type,
requiring immutable reference to corresponding
<code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_UnderwriterCapability">UnderwriterCapability</a></code> for the market, and <code>base_type</code>
descriptor.

See inner function <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_market_internal">register_market_internal</a>()</code>.


<a id="@Aborts_70"></a>

### Aborts


* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_GENERIC_TOO_FEW_CHARACTERS">E_GENERIC_TOO_FEW_CHARACTERS</a></code>: Asset descriptor is too short.
* <code><a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_E_GENERIC_TOO_MANY_CHARACTERS">E_GENERIC_TOO_MANY_CHARACTERS</a></code>: Asset descriptor is too long.


<a id="@Testing_71"></a>

### Testing


* <code>test_register_market_base_generic_internal()</code>
* <code>test_register_market_generic_name_too_few()</code>
* <code>test_register_market_generic_name_too_many()</code>


<pre><code><b>public</b>(<b>friend</b>) <b>fun</b> <a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_register_market_base_generic_internal">register_market_base_generic_internal</a>&lt;QuoteCoinType, UtilityCoinType&gt;(base_name_generic: <a href="_String">string::String</a>, lot_size: u64, tick_size: u64, min_size: u64, underwriter_capability_ref: &<a href="registry.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_registry_UnderwriterCapability">registry::UnderwriterCapability</a>, utility_coins: <a href="_Coin">coin::Coin</a>&lt;UtilityCoinType&gt;): u64
</code></pre>
