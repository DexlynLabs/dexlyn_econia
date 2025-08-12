
<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_resource_account"></a>

# Module `0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450::resource_account`

Manages an Econia-owned resource account.


-  [Resource `SignerCapabilityStore`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_resource_account_SignerCapabilityStore)
-  [Function `get_address`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_resource_account_get_address)
    -  [Testing](#@Testing_0)
-  [Function `get_signer`](#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_resource_account_get_signer)
    -  [Testing](#@Testing_1)


<pre><code><b>use</b> <a href="">0x1::account</a>;
<b>use</b> <a href="">0x1::bcs</a>;
<b>use</b> <a href="">0x1::timestamp</a>;
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_resource_account_SignerCapabilityStore"></a>

## Resource `SignerCapabilityStore`

Stores a signing capability for the Econia resource account.


<pre><code><b>struct</b> <a href="resource_account.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_resource_account_SignerCapabilityStore">SignerCapabilityStore</a> <b>has</b> key
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_resource_account_get_address"></a>

## Function `get_address`

Return resource account address.


<a id="@Testing_0"></a>

### Testing


* <code>test_mixed()</code>


<pre><code>#[view]
<b>public</b>(<b>friend</b>) <b>fun</b> <a href="resource_account.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_resource_account_get_address">get_address</a>(): <b>address</b>
</code></pre>



<a id="0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_resource_account_get_signer"></a>

## Function `get_signer`

Return resource account signer.


<a id="@Testing_1"></a>

### Testing


* <code>test_mixed()</code>


<pre><code><b>public</b>(<b>friend</b>) <b>fun</b> <a href="resource_account.md#0x7b00569d23c3edd4538d0b6d8db15dd9f9c07e5d830f35b46afbaa670923b450_resource_account_get_signer">get_signer</a>(): <a href="">signer</a>
</code></pre>
