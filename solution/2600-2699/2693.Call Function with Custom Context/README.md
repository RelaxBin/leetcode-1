# [2693. Call Function with Custom Context](https://leetcode.cn/problems/call-function-with-custom-context)

[English Version](/solution/2600-2699/2693.Call%20Function%20with%20Custom%20Context/README_EN.md)

## 题目描述

<!-- 这里写题目描述 -->

<p>Enhance all functions to have the&nbsp;<code>callPolyfill</code>&nbsp;method. The method accepts an object&nbsp;<code>obj</code>&nbsp;as it&#39;s first parameter and any number of additional arguments. The&nbsp;<code>obj</code>&nbsp;becomes the&nbsp;<code>this</code>&nbsp;context for the function. The additional arguments are passed to the function (that the <code>callPolyfill</code>&nbsp;method belongs on).</p>

<p>For example if you had the function:</p>

<pre>
function tax(price, taxRate) {
  const totalCost = price * (1 + taxRate);
&nbsp; console.log(`The cost of ${this.item} is ${totalCost}`);
}
</pre>

<p>Calling this function like&nbsp;<code>tax(10, 0.1)</code>&nbsp;will log&nbsp;<code>&quot;The cost of undefined is 11&quot;</code>. This is because the&nbsp;<code>this</code>&nbsp;context was not defined.</p>

<p>However, calling the function like&nbsp;<code>tax.callPolyfill({item: &quot;salad&quot;}, 10, 0.1)</code>&nbsp;will log&nbsp;<code>&quot;The cost of salad is 11&quot;</code>. The&nbsp;<code>this</code>&nbsp;context was appropriately set, and the function logged an appropriate output.</p>

<p>Please solve this without using&nbsp;the built-in&nbsp;<code>Function.call</code>&nbsp;method.</p>

<p>&nbsp;</p>
<p><strong class="example">Example 1:</strong></p>

<pre>
<strong>Input:</strong>
fn = function add(b) {
  return this.a + b;
}
args = [{&quot;a&quot;: 5}, 7]
<strong>Output:</strong> 12
<strong>Explanation:</strong>
fn.callPolyfill({&quot;a&quot;: 5}, 7); // 12
callPolyfill sets the &quot;this&quot; context to {&quot;a&quot;: 5}. 7 is passed as an argument.
</pre>

<p><strong class="example">Example 2:</strong></p>

<pre>
<strong>Input:</strong> 
fn = function tax(price, taxRate) { 
&nbsp;return `The cost of the ${this.item} is ${price * taxRate}`; 
}
args = [{&quot;item&quot;: &quot;burger&quot;}, 10, 1,1]
<strong>Output:</strong> &quot;The cost of the burger is 11&quot;
<strong>Explanation:</strong> callPolyfill sets the &quot;this&quot; context to {&quot;item&quot;: &quot;burger&quot;}. 10 and 1.1 are passed as additional arguments.
</pre>

<p>&nbsp;</p>
<p><strong>Constraints:</strong></p>

<ul style="list-style-type:square;">
	<li><code><font face="monospace">typeof args[0] == &#39;object&#39; and args[0] != null</font></code></li>
	<li><code>1 &lt;= args.length &lt;= 100</code></li>
	<li><code>2 &lt;= JSON.stringify(args[0]).length &lt;= 10<sup>5</sup></code></li>
</ul>

## 解法

<!-- 这里可写通用的实现逻辑 -->

<!-- tabs:start -->

### **TypeScript**

<!-- 这里可写当前语言的特殊实现逻辑 -->

```ts

```

<!-- tabs:end -->