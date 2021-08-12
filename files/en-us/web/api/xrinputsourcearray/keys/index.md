---
title: XRInputSourceArray.keys()
slug: Web/API/XRInputSourceArray/keys
tags:
- API
- AR
- Devices
- Input Sources
- Inputs
- Iterator
- Method
- Mixed
- Reality
- Reference
- Sources
- VR
- Virtual
- WebXR
- WebXR API
- WebXR Device API
- XR
- XRInputSourceArray
- augmented
- keys
browser-compat: api.XRInputSourceArray.keys
---
<p>{{APIRef("WebXR Device API")}}</p>

<p>The <code><strong>keys()</strong></code> method in the
  {{domxref("XRInputSourceArray")}} interface returns a {{Glossary("JavaScript")}}
  <code><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Iterator">iterator</a></code>
  which can then be used to iterate over the keys used to reference each item in the array
  of input sources.</p>

<h2 id="Syntax">Syntax</h2>

<pre class="brush: js"><em>xrInputSourceArray</em>.keys();
</pre>

<h3 id="Parameters">Parameters</h3>

<p>None.</p>

<h3 id="Return_value">Return value</h3>

<p>A
  JavaScript <code><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Iterator">iterator</a></code> that
  can be used to walk through the keys for each entry in the list of input sources. The
  values returned by the iterator are the indexes of each entry in the list; that is, the
  numbers 0, 1, 2, and so forth through the index of the last item in the list.</p>

<h2 id="Examples">Examples</h2>

<p>This example snippet gets the list of inputs for a session and tries to handle each
  type of input device it supports using.</p>

<pre class="brush: js">for (const inputIdx of xrSession.inputSources.keys()) {
  /* the keys are the indexes into the list of inputs */
  checkInput(xrSession.inputSources[inputIdx]);
}
</pre>

<p>Here,
  <code><a href="/en-US/docs/Web/JavaScript/Reference/Statements/for...of">for...of</a></code>
  is used to iterate over each of the keys. For each key, the input is retrieved using the
  index with array notation: <code>xrSession.inputSources[inputIdx]</code>.</p>

<h2 id="Specifications">Specifications</h2>

{{Specifications}}

<h2 id="Browser_compatibility">Browser compatibility</h2>

<p>{{Compat}}</p>

<h2 id="See_also">See also</h2>

<ul>
  <li><a href="/en-US/docs/Web/API/WebXR_Device_API/Inputs">Inputs and input sources</a>
  </li>
  <li>The {{domxref("XRInputSourceArray")}} method {{domxref("XRInputSourceArray.values",
    "values()")}}</li>
  <li>The
    <code><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array">Array</a></code> method <code><a href="/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/keys">keys(</a>)</code>
  </li>
  <li>{{domxref("XRInputSource")}}</li>
</ul>