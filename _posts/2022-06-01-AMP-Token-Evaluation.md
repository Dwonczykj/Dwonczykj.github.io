---
created: May 25, 2022 11:38 AM
entities: AMP, Flexa
layout: post_notion
title: Payments without the fees (AMP Token)
excerpt: In this article, I discuss a decentralised technology that seeks to radically improve the process of paying and save merchants hundreds of billions of dollars each year
categories: [Payments, Crypto]
comments: true
---
<html>
<head>
<style>
    figure {
        margin: 1.25em 0;
        page-break-inside: avoid;
    }

    figcaption {
        opacity: 0.5;
        font-size: 85%;
        margin-top: 0.5em;
    }

    mark {
        background-color: transparent;
    }

    .indented {
        padding-left: 1.5em;
    }

    hr {
        background: transparent;
        display: block;
        width: 100%;
        height: 1px;
        visibility: visible;
        border: none;
        border-bottom: 1px solid rgba(55, 53, 47, 0.09);
    }

    img {
        max-width: 100%;
    }

    @media only print {
        img {
            max-height: 100vh;
            object-fit: contain;
        }
    }

    @page {
        margin: 1in;
    }

    .collection-content {
        font-size: 0.875rem;
    }

    .column-list {
        display: flex;
        justify-content: space-between;
    }

    .column {
        padding: 0 1em;
    }

    .column:first-child {
        padding-left: 0;
    }

    .column:last-child {
        padding-right: 0;
    }

    .table_of_contents-item {
        display: block;
        font-size: 0.875rem;
        line-height: 1.3;
        padding: 0.125rem;
    }

    .table_of_contents-indent-1 {
        margin-left: 1.5rem;
    }

    .table_of_contents-indent-2 {
        margin-left: 3rem;
    }

    .table_of_contents-indent-3 {
        margin-left: 4.5rem;
    }

    .table_of_contents-link {
        text-decoration: none;
        opacity: 0.7;
        border-bottom: 1px solid rgba(55, 53, 47, 0.18);
    }

    table,
    th,
    td {
        border: 1px solid rgba(55, 53, 47, 0.09);
        border-collapse: collapse;
    }

    table {
        border-left: none;
        border-right: none;
    }

    th,
    td {
        font-weight: normal;
        padding: 0.25em 0.5em;
        line-height: 1.5;
        min-height: 1.5em;
        text-align: left;
    }

    th {
        color: rgba(55, 53, 47, 0.6);
    }

    ol,
    ul {
        margin: 0;
        margin-block-start: 0.6em;
        margin-block-end: 0.6em;
    }

    li > ol:first-child,
    li > ul:first-child {
        margin-block-start: 0.6em;
    }

    ul > li {
        list-style: disc;
    }

    ul.to-do-list {
        text-indent: -1.7em;
    }

    ul.to-do-list > li {
        list-style: none;
    }

    .to-do-children-checked {
        text-decoration: line-through;
        opacity: 0.375;
    }

    ul.toggle > li {
        list-style: none;
    }

    ul {
        padding-inline-start: 1.7em;
    }

    ul > li {
        padding-left: 0.1em;
    }

    ol {
        padding-inline-start: 1.6em;
    }

    ol > li {
        padding-left: 0.2em;
    }

    .mono ol {
        padding-inline-start: 2em;
    }

    .mono ol > li {
        text-indent: -0.4em;
    }

    .toggle {
        padding-inline-start: 0em;
        list-style-type: none;
    }

    /* Indent toggle children */
    .toggle > li > details {
        padding-left: 1.7em;
    }

    .toggle > li > details > summary {
        margin-left: -1.1em;
    }

    .selected-value {
        display: inline-block;
        padding: 0 0.5em;
        background: rgba(206, 205, 202, 0.5);
        border-radius: 3px;
        margin-right: 0.5em;
        margin-top: 0.3em;
        margin-bottom: 0.3em;
        white-space: nowrap;
    }

    .collection-title {
        display: inline-block;
        margin-right: 1em;
    }

    .simple-table {
        margin-top: 1em;
        font-size: 0.875rem;
        empty-cells: show;
    }
    .simple-table td {
        height: 29px;
        min-width: 120px;
    }

    .simple-table th {
        height: 29px;
        min-width: 120px;
    }

    .simple-table-header-color {
        background: rgb(247, 246, 243);
        color: black;
    }
    .simple-table-header {
        font-weight: 500;
    }

    time {
        opacity: 0.5;
    }

    .icon {
        display: inline-block;
        max-width: 1.2em;
        max-height: 1.2em;
        text-decoration: none;
        vertical-align: text-bottom;
        margin-right: 0.5em;
    }

    img.icon {
        border-radius: 3px;
    }

    .user-icon {
        width: 1.5em;
        height: 1.5em;
        border-radius: 100%;
        margin-right: 0.5rem;
    }

    .user-icon-inner {
        font-size: 0.8em;
    }

    .text-icon {
        border: 1px solid #000;
        text-align: center;
    }

    .page-cover-image {
        display: block;
        object-fit: cover;
        width: 100%;
        max-height: 30vh;
    }

    .page-header-icon {
        font-size: 3rem;
        margin-bottom: 1rem;
    }

    .page-header-icon-with-cover {
        margin-top: -0.72em;
        margin-left: 0.07em;
    }

    .page-header-icon img {
        border-radius: 3px;
    }

    .link-to-page {
        margin: 1em 0;
        padding: 0;
        border: none;
        font-weight: 500;
    }

    p > .user {
        opacity: 0.5;
    }

    td > .user,
    td > time {
        white-space: nowrap;
    }

    input[type="checkbox"] {
        transform: scale(1.5);
        margin-right: 0.6em;
        vertical-align: middle;
    }

    p {
        margin-top: 0.5em;
        margin-bottom: 0.5em;
    }

    .image {
        border: none;
        margin: 1.5em 0;
        padding: 0;
        border-radius: 0;
        text-align: center;
    }

    .code,
    code {
        background: rgba(135, 131, 120, 0.15);
        border-radius: 3px;
        padding: 0.2em 0.4em;
        border-radius: 3px;
        font-size: 85%;
        tab-size: 2;
    }

    code {
        color: #eb5757;
    }

    .code {
        padding: 1.5em 1em;
    }

    .code-wrap {
        white-space: pre-wrap;
        word-break: break-all;
    }

    .code > code {
        background: none;
        padding: 0;
        font-size: 100%;
        color: inherit;
    }

    blockquote {
        font-size: 1.25em;
        margin: 1em 0;
        padding-left: 1em;
        border-left: 3px solid rgb(55, 53, 47);
    }

    .bookmark {
        text-decoration: none;
        max-height: 8em;
        padding: 0;
        display: flex;
        width: 100%;
        align-items: stretch;
    }

    .bookmark-title {
        font-size: 0.85em;
        overflow: hidden;
        text-overflow: ellipsis;
        height: 1.75em;
        white-space: nowrap;
    }

    .bookmark-text {
        display: flex;
        flex-direction: column;
    }

    .bookmark-info {
        flex: 4 1 180px;
        padding: 12px 14px 14px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    .bookmark-image {
        width: 33%;
        flex: 1 1 180px;
        display: block;
        position: relative;
        object-fit: cover;
        border-radius: 1px;
    }

    .bookmark-description {
        color: rgba(55, 53, 47, 0.6);
        font-size: 0.75em;
        overflow: hidden;
        max-height: 4.5em;
        word-break: break-word;
    }

    .bookmark-href {
        font-size: 0.75em;
        margin-top: 0.25em;
    }

    .sans { font-family: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol"; }
    .code { font-family: "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace; }
    .serif { font-family: Lyon-Text, Georgia, ui-serif, serif; }
    .mono { font-family: iawriter-mono, Nitti, Menlo, Courier, monospace; }
    .pdf .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK JP'; }
    .pdf:lang(zh-CN) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC'; }
    .pdf:lang(zh-TW) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK TC'; }
    .pdf:lang(ko-KR) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK KR'; }
    .pdf .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
    .pdf:lang(zh-CN) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
    .pdf:lang(zh-TW) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
    .pdf:lang(ko-KR) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
    .pdf .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK JP'; }
    .pdf:lang(zh-CN) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK SC'; }
    .pdf:lang(zh-TW) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK TC'; }
    .pdf:lang(ko-KR) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK KR'; }
    .pdf .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
    .pdf:lang(zh-CN) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
    .pdf:lang(zh-TW) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
    .pdf:lang(ko-KR) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
    .highlight-default {
        color: rgba(55, 53, 47, 1);
    }
    .highlight-gray {
        color: rgba(120, 119, 116, 1);
        fill: rgba(120, 119, 116, 1);
    }
    .highlight-brown {
        color: rgba(159, 107, 83, 1);
        fill: rgba(159, 107, 83, 1);
    }
    .highlight-orange {
        color: rgba(217, 115, 13, 1);
        fill: rgba(217, 115, 13, 1);
    }
    .highlight-yellow {
        color: rgba(203, 145, 47, 1);
        fill: rgba(203, 145, 47, 1);
    }
    .highlight-teal {
        color: rgba(68, 131, 97, 1);
        fill: rgba(68, 131, 97, 1);
    }
    .highlight-blue {
        color: rgba(51, 126, 169, 1);
        fill: rgba(51, 126, 169, 1);
    }
    .highlight-purple {
        color: rgba(144, 101, 176, 1);
        fill: rgba(144, 101, 176, 1);
    }
    .highlight-pink {
        color: rgba(193, 76, 138, 1);
        fill: rgba(193, 76, 138, 1);
    }
    .highlight-red {
        color: rgba(212, 76, 71, 1);
        fill: rgba(212, 76, 71, 1);
    }
    .highlight-gray_background {
        background: rgba(241, 241, 239, 1);
    }
    .highlight-brown_background {
        background: rgba(244, 238, 238, 1);
    }
    .highlight-orange_background {
        background: rgba(251, 236, 221, 1);
    }
    .highlight-yellow_background {
        background: rgba(251, 243, 219, 1);
    }
    .highlight-teal_background {
        background: rgba(237, 243, 236, 1);
    }
    .highlight-blue_background {
        background: rgba(231, 243, 248, 1);
    }
    .highlight-purple_background {
        background: rgba(244, 240, 247, 0.8);
    }
    .highlight-pink_background {
        background: rgba(249, 238, 243, 0.8);
    }
    .highlight-red_background {
        background: rgba(253, 235, 236, 1);
    }
    .block-color-default {
        color: inherit;
        fill: inherit;
    }
    .block-color-gray {
        color: rgba(120, 119, 116, 1);
        fill: rgba(120, 119, 116, 1);
    }
    .block-color-brown {
        color: rgba(159, 107, 83, 1);
        fill: rgba(159, 107, 83, 1);
    }
    .block-color-orange {
        color: rgba(217, 115, 13, 1);
        fill: rgba(217, 115, 13, 1);
    }
    .block-color-yellow {
        color: rgba(203, 145, 47, 1);
        fill: rgba(203, 145, 47, 1);
    }
    .block-color-teal {
        color: rgba(68, 131, 97, 1);
        fill: rgba(68, 131, 97, 1);
    }
    .block-color-blue {
        color: rgba(51, 126, 169, 1);
        fill: rgba(51, 126, 169, 1);
    }
    .block-color-purple {
        color: rgba(144, 101, 176, 1);
        fill: rgba(144, 101, 176, 1);
    }
    .block-color-pink {
        color: rgba(193, 76, 138, 1);
        fill: rgba(193, 76, 138, 1);
    }
    .block-color-red {
        color: rgba(212, 76, 71, 1);
        fill: rgba(212, 76, 71, 1);
    }
    .block-color-gray_background {
        background: rgba(241, 241, 239, 1);
    }
    .block-color-brown_background {
        background: rgba(244, 238, 238, 1);
    }
    .block-color-orange_background {
        background: rgba(251, 236, 221, 1);
    }
    .block-color-yellow_background {
        background: rgba(251, 243, 219, 1);
    }
    .block-color-teal_background {
        background: rgba(237, 243, 236, 1);
        color: rgba(10, 10, 10, 1);
    }
    .block-color-blue_background {
        background: rgba(231, 243, 248, 1);
    }
    .block-color-purple_background {
        background: rgba(244, 240, 247, 0.8);
    }
    .block-color-pink_background {
        background: rgba(249, 238, 243, 0.8);
    }
    .block-color-red_background {
        background: rgba(253, 235, 236, 1);
    }
    .select-value-color-pink { background-color: rgba(245, 224, 233, 1); }
    .select-value-color-purple { background-color: rgba(232, 222, 238, 1); }
    .select-value-color-green { background-color: rgba(219, 237, 219, 1); }
    .select-value-color-gray { background-color: rgba(227, 226, 224, 1); }
    .select-value-color-opaquegray { background-color: rgba(255, 255, 255, 0.0375); }
    .select-value-color-orange { background-color: rgba(250, 222, 201, 1); }
    .select-value-color-brown { background-color: rgba(238, 224, 218, 1); }
    .select-value-color-red { background-color: rgba(255, 226, 221, 1); }
    .select-value-color-yellow { background-color: rgba(253, 236, 200, 1); }
    .select-value-color-blue { background-color: rgba(211, 229, 239, 1); }

    .checkbox {
        display: inline-flex;
        vertical-align: text-bottom;
        width: 16;
        height: 16;
        background-size: 16px;
        margin-left: 2px;
        margin-right: 5px;
    }

    .checkbox-on {
        background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20width%3D%2216%22%20height%3D%2216%22%20fill%3D%22%2358A9D7%22%2F%3E%0A%3Cpath%20d%3D%22M6.71429%2012.2852L14%204.9995L12.7143%203.71436L6.71429%209.71378L3.28571%206.2831L2%207.57092L6.71429%2012.2852Z%22%20fill%3D%22white%22%2F%3E%0A%3C%2Fsvg%3E");
    }

    .checkbox-off {
        background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20x%3D%220.75%22%20y%3D%220.75%22%20width%3D%2214.5%22%20height%3D%2214.5%22%20fill%3D%22white%22%20stroke%3D%22%2336352F%22%20stroke-width%3D%221.5%22%2F%3E%0A%3C%2Fsvg%3E");
    }

    .responsive-iframe-container {
        position: relative;
        overflow: hidden;
        width: 100%;
        padding-top: 56.25%; /* 16:9 Aspect Ratio (divide 9 by 16 = 0.5625) */
    }

    .responsive-iframe-container>.responsive-iframe {
        position: absolute;
        top: 0;
        left: 0;
        bottom: 0;
        right: 0;
        width: 100%;
        height: 100%;
    }
	
</style>
</head>
<body><article id="43281ec4-c345-4ff8-8e9e-ca924a8fd710" class="page sans">

<div class="page-body"><p id="467c0f06-548e-4282-b092-caa4866df8c0" class="">In this article, I discuss AMP, a Crypto ERC20 compatible token that seeks to radically improve the process of paying and save merchants hundreds of billions of dollars each year.</p><p id="421f5903-3f33-4ddb-8522-9f3b8fa473bf" class="">I mainly verbalise my notes from reading AMP’s Whitepaper (the specification and intention of the coin from its creators), with the addition of other sources such as the interviews and speeches from the founders.</p><p id="c4091779-69d7-46fe-9456-869a4c66ae34" class="">I begin with a higher level overview of the intended direction and goals of the AMP token and its coupled network, Flexa. I then present a more in depth analysis of the tokens architecture and characteristics using a mind map as this more clearly denotes the connections between the various parts of the revolutionary Flexa payments ecosystem and the design of the AMP token.</p><h1 id="dd12e824-768e-450b-bf96-95ee8c36daac" class="">Description</h1><p id="04506ee0-404d-4102-b0b0-67f03d7e0b20" class=""><mark class="highlight-pink">AMP</mark> is a <mark class="highlight-orange">collateral token</mark>. And a token? A cryptocurrency token is like a chip on a poker table, it represents an asset (i.e. $5 of gambling power on the poker table) or a specific use and is stored on a blockchain.</p><p id="a427860c-34bb-4e7d-a617-db97bf9dad08" class="">It exists to act as collateral for financial transactions where traditionally, bonds, money etc would be used and be held by custodians (third parties) all charging fees for their services.</p><h2 id="e4f31af8-2d1b-4139-afb9-3b91320faddc" class="">Mission Statement </h2><p id="b4309d48-f6db-452f-b813-d16aca5b8510" class="">Its goal is to reduce counterparty risk on transactions through <strong>financially efficient</strong> collateralization.</p><h1 id="052c2db3-98b3-4580-9b72-28617e09b698" class="">Design Overview</h1><p id="b9134ca8-bedc-4e25-a89d-d82e703afa88" class="">AMP enables tokens to be conditionally allocated as collateral <strong>without requiring additional transfers</strong> to another smart contract to store the collateral for the transaction. This is cheaper and removes this custody risk, whereby collateral tokens need to be temporarily transferred between smart contracts to act as collateral.</p><p id="a5661101-7ebd-44c4-b377-47401926ac90" class="">AMP has been designed using economics fundamentals models to ensure that the token is low volatility and hence suitable for collateralization due to the economic surety of its value over the lifetime of a transaction. AMP’s value compounds, exclusively as a result of any utility that it provides. This means that the more transactions that it collateralises, the more valuable the collateral that is used. This feedback loop is described in the white paper abstract as a ‘<mark class="highlight-yellow"><em>virtuous feedback loop</em></mark><em> of increasing spending capacity</em>’. Additionally, using a decentralised architecture significantly reduces fees traditionally charged by collateral custodians in financial systems via <mark class="highlight-yellow">open validator sets</mark> and <mark class="highlight-yellow">distributed convergence mechanisms</mark>.</p><p id="118aa936-c028-405a-8f36-8e8ebeeb7e4a" class="">To put in perspective the cost to society currently for the cost to make a payment, its estimated (see <a href="https://youtu.be/32_3fUPJJVA?t=1178">https://youtu.be/32_3fUPJJVA?t=1178</a>) at 2% of US GDP vs the entire US Military defence budget which is 3% of US GDP.</p><h1 id="4aab2d94-13a5-410b-bca3-d8e2b681c325" class="">Digital Payments</h1><figure id="87a0689f-5e6a-4a04-93bd-c13486e02428" class="link-to-page"><a href="https://www.notion.so/Flexa-87a0689f5e6a4a0493bdc13486e02428"><img class="icon" src="https://flexa.network/favicon-32x32.png?v=6605a38c3c1982c90dd3353d4c43250e"/>Flexa</a></figure><p id="015a8809-b91f-4353-810e-6dcf3605387f" class=""><mark class="highlight-orange">Flexa</mark> integrates natively with existing point of sale (POS) systems<style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mrow></mrow><mn>9</mn></msup></mrow><annotation encoding="application/x-tex">^{9}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.8141079999999999em;vertical-align:0em;"></span><span class="mord"><span></span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141079999999999em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">9</span></span></span></span></span></span></span></span></span></span></span></span></span><span>﻿</span></span> and online platforms to enable payment in a typical checkout experience. The network Spend SDK is permissionless; mobile wallets or applications can create unique, interoperable authorisation codes for conveyance.<style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mrow></mrow><mn>10</mn></msup></mrow><annotation encoding="application/x-tex">^{10}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.8141079999999999em;vertical-align:0em;"></span><span class="mord"><span></span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141079999999999em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">10</span></span></span></span></span></span></span></span></span></span></span></span></span><span>﻿</span></span></p><h2 id="99ef855b-f868-4cc5-be9d-72251588fa4b" class="">Digital collateral providers &amp; their incentive</h2><p id="e67b047f-1b75-45da-affa-68391927fe62" class="">To enable payment functionality, applications and communities can collectively stake AMP tokens on behalf of users. As incentive for supplying collateral, the entirety of network transaction revenue funds the continuous open-market purchase of AMP tokens for redistribution as network rewards.
</p><figure class="block-color-teal_background callout" style="white-space:pre-wrap;display:flex" id="f58a9a96-5738-4257-99a9-d67d692aec33"><div style="font-size:1.5em"><span class="icon">📘</span></div><div style="width:100%">Numeraire Good → A good that acts a base point of reference value for a good’s market.
• <em>A numeraire is usually applied to a single good, which becomes the base value for the entire index or market.
• The U.S. dollar remains the numeraire for most commodity prices.</em></div></figure><p id="ae49f75d-6755-41b1-a7ff-69660692a54a" class="">The following link from original conference note reasons why collateral is needed for permissionless payments:</p>
<figure id="368d5b6e-c0c6-4232-86bf-36a0836483c5"><a href="https://youtu.be/XaXbl-og23o?t=1423" class="bookmark source"><div class="bookmark-info"><div class="bookmark-text"><div class="bookmark-title">FLEXA: HODL. BUIDL. SPEDN! [Sponsored] | Consensus 2019</div></div><div class="bookmark-href"><img src="https://www.google.com/favicon.ico" class="icon bookmark-icon"/>https://youtu.be/XaXbl-og23o?t=1423</div></div><img src="https://i.ytimg.com/vi/XaXbl-og23o/hqdefault.jpg" class="bookmark-image"/></a></figure>
<p>which is supported by the below diagram that reveals the size of the interchange payments ecosystem:</p>
<figure id="93575bb7-fd2d-4b26-bf90-c07690c36770" class="image"><a href="point-of-sale.png"><img style="width:60%" src="point-of-sale.png"/></a></figure>
<h1 id="7ee7dbba-d6d4-4ef9-bf1e-36113dc9ca11" class="">AMP token description</h1><p id="f1e736ee-0c88-40c7-8c7d-674806dfb48c" class="">AMP resembles a rudimentary token in that balances are assigned to Ethereum addresses, but the <mark class="highlight-pink">tokens also belong to a particular 32-byte partition</mark> which effectively serves as a second-dimension in the distribution array of the balances. (i.e. we can see how much token there is for a particular <mark class="highlight-pink">ethereum address</mark>, but we can also see how much token there is on any specified address to a <mark class="highlight-pink">32-byte partition of memory</mark>.</p><p id="2d839d40-ff86-43ea-847d-40ce5fded654" class="">AMP supports transfers between addresses and partitions through the <code>transferByPartition</code>
function, and includes the <code>approveByPartition</code> function that authorises an address to transfer
tokens on behalf of the caller, but only from a particular partition.</p><p id="5b8bfe7f-7f82-4c84-8a47-0f38906f8ea0" class="">For backwards compatibility of the ERC20 token, the token must support the <code>transfer</code> and <code>approve</code> contract functions. To do this, it uses the <mark class="highlight-pink">zero partition</mark> (”default partition”) with address of x0.</p><p id="75658f84-7adf-4e29-9da6-6aeab9a6b63b" class="">We can think of partition as its location on the chain storage and address as the address of the ethereum wallet holding it perhaps.</p><figure id="a36ebc3d-56e4-4715-9732-d98a574f414b" class="image"><a href="partition-semantics.png"><img style="width:1192px" src="partition-semantics.png"/></a></figure><p id="998cd211-95a2-4be6-ab56-1a17267c8352" class="">For every transfer, 2 events are emitted from the smart contract so that balances can be tracked off the chain too (i.e. without having to aggregate all transactions since genesis block to know balances). These events are:</p><ul id="d15b5ef4-fafe-433a-9369-1749c070806c" class="bulleted-list"><li style="list-style-type:disc"><code>Transfer</code> containing the to, from address and the amount</li></ul><ul id="48bf111e-8c76-45ac-af93-8053aea4e2b0" class="bulleted-list"><li style="list-style-type:disc"><code>TransferByPartition</code> contains the same data as Transfer, as well as the to and from
partitions and any metadata or operatorData parameters.</li></ul>
<h2 id="56fa149b-c3d6-455f-83c6-c8438da0c014" class="">AMP’s Unique Differentiator</h2><p id="6418a8fd-eddb-4cab-aabc-c058ac2e27cc" class="">The partition. I go into depth on what this is and why it is so powerful in the next section that links together all aspects of the design. For developers, the key interface is:</p><figure class="block-color-gray_background callout" style="white-space:pre-wrap;display:flex" id="a85ba2da-c883-4cb3-9ae6-ab8b3bf86755"><div style="font-size:1.5em"><span class="icon">🤔</span></div><div style="width:100%"><code>IAmpPartitionStrategyValidator</code></div></figure><p id="1aebec57-4c27-4f67-9367-135bc7c501d5" class="">
</p><h1 id="690f019c-9095-4c16-a11d-313171499321" class="block-color-purple">In-depth Architecture Evaluation</h1><p id="f434af4e-91e6-4716-abde-fb2ddbc3277b" class="">The below is an in depth look at the architecture of the AMP token as described in the AMP Whitepaper. It reiterates the implementation description of the AMP token that we have just covered. The graph then goes into far more detail answering questions such as “<em>Why is the AMP token has this design?</em>”, “<em>How does this tie in to the Flexa payments pipe network?</em>” and “<em>How can blockchain DApp developers leverage the functionality of the AMP token (contract) for their own use-cases and applications in the payments ecosystem?</em>”.</p>

<div class="responsive-iframe-container"><iframe class="responsive-iframe" style="border:none" src="https://whimsical.com/embed/TM67rPRGs5boowrueSZ2oN@2Ux7TurymMZ8y6zPcGwk"></iframe></div>

<p id="47797c0e-cff5-4bfd-86fa-c523e05317ae" class="">The next section displays an overview of the different participants in a payments network and how they interact with one another. This is useful for understanding the role of the Flexa network and its AMP token in the worldwide payments ecosystem.</p>

<div class="responsive-iframe-container"><iframe class="responsive-iframe" style="border:none" src="https://whimsical.com/embed/M7bqDoDFCJrh7WsumZ8ck2"></iframe></div>
<br>

<h1 id="e9fcb3b4-cea7-4bc3-addc-ba45c1b161f6" class="">Exchange spread costs at point-of-sale</h1>
<h2 id="b9ad83f8-2c51-49a5-9f2a-be354a9dcf2b" class="">Understanding the cost</h2>
<p id="e7672e24-b152-4aa4-81cb-7d0f34e9d0d5" class="">In any market for a given asset, there are those who wish to sell that asset and those who wish to buy it. In general, those who wish to sell would rather a higher price and those who wish to buy would rather a cheaper price. For example, when you buy a house, the seller would probably rather you pay over asking price, but you would probably rather pay below. This meeting in the middle or agreeing on a price is the function of the marketplace. It facilitates the bargaining process for the transfer of the asset (the house in our example) between buyers and sellers.</p><p id="d49f6c07-8b75-4489-a579-7ebbc8929a35" class="">Let’s take a look at an another example to isolate the potential cost of this process for both or either of the buyer and seller. Imagine you want to purchase an ounce of gold for £1,500. There are a few dealers you can go to and you choose the one offering an ounce of gold for the cheapest price of £1,600. You then begin the process of bargaining to see if the dealer will sell for £1,500 and the dealer wants to know if they can get you up to £1,600. After negotiations, you agree to pay £1,560 for the gold. COST. The purchase costs you £60 because you received what you value as £1,500 of gold but paid £1,560 for it. The sale costs the dealer £40 because they value the gold at £1,600, but agreed to sell it to you for £1,560. Here we see the cost of the trade for both parties in the transaction, the cost of the exchange.</p><p id="00d700db-cd8c-493b-877e-cc99c710ff8d" class="">Now back to decentralised payments. What are the costs to the merchant and the consumer for paying in 2 different assets, assets that need to be exchanged for one another in a transaction like the one above?</p><p id="2148ce09-77e4-467b-8b14-e2766c2a3c8d" class="">To answer this question, I explain the way a payment works using an example application built on the Flexa network. </p>
<h2 id="98b5d085-cadc-498a-a0d4-e027bf2efdd0" class="">Existing Flexa Pay Apps</h2>
<p id="843f3447-926a-4d58-86eb-1879526baf2e" class=""><strong><mark class="highlight-pink">SPEDN</mark></strong> is an App built by the Flexa team to allow users to pay over the Flexa network. <strong><mark class="highlight-pink">SPEDN</mark></strong> uses Gemini Exchange behind the scenes to facilitate the exchange of the payment asset to the merchants chosen payment asset. In addition, all cryptocurrency deposited on the <strong><mark class="highlight-pink">SPEDN</mark></strong> mobile app is custodied with Gemini, providing security for those using this new payment technology.</p>
<p id="0a6b5af4-15ca-4838-8160-fd6650adcfae" class="">
So let’s assume I want to pay for a coffee using the Flexa app with the BitCoin that I have stored in the app, how is my BTC exchanged for USD? Say the coffee costs $3. When you scan the register to pay for the coffee, the app sells $3 worth of BTC (behind the scenes) for you at the current market <mark class="highlight-red">ask (buy) </mark>price. Selling the BTC at the ask price means that you make market by <mark class="highlight-orange">paying the bid-ask spread</mark> (<mark class="highlight-red">the cost or fee for exchange</mark>) in the BTC/USD spot market on the gemini exchange. As you exchange at the current market ask (buy) price, it is therefore important users have the option to use exchange with <mark class="highlight-orange">low-volatility</mark> digital assets to avoid making this exchange at a poor price relative to the current market mid price.</p>

<h3>Can a merchant end up paying for the volatility of the consumers chosen payment asset?</h3>

<p>Here, we are talking about a situation in which, the consumer wants to pay with ETH and the merchant wants to receive their payment in GBP (<i>a reasonable default case</i>). 

In this scenario, could the merchant end up paying higher fees for the transaction, purely because the customer paid with a volatile asset such as ETH which is the customer’s choice and outside of the control of the merchant?

To avoid this potential risk for merchants, the consumers ETH is exchanged for the exact price of the item in GBP set by the merchant, so that regardless of the price of the exchange, the same GBP price is always paid to the merchant and the volatility market risk of the ETH payment is taken on entirely by the customer.</p>

<h3>Reviews</h3>

<p id="c41aeada-73e4-4f66-bf9e-353dfc1a3745" class="">Back to reality, how have real people found this process?</p><p id="17ad03ef-5e0c-450e-8800-007db38ff403" class=""><em>The following statements are taken from a review in March 2021 on the app store landing page: </em><em><a href="https://apps.apple.com/us/app/spedn-by-flexa/id1456135087">SPEDN by Flexa on the App Store (apple.com)</a></em><em> - Reviews </em><em><strong>99dc99, </strong></em><em><strong><time>@March 3, 2021 8:31 PM</time></strong></em><em><strong> titled - </strong></em><mark class="highlight-yellow"><em><strong>I can spend my crypto fee-free finally!</strong></em></mark></p><blockquote id="cf3bf5d5-cada-457b-adf3-10d6f650f2a3" class="">It just <strong><mark class="highlight-orange">transacts the value of the crypto at the time I scan at the register</mark></strong>. 

I think (<mark class="highlight-gray">you can only transfer</mark><em>)</em> one way to the wallet right now (<mark class="highlight-gray">i.e. cannot withdraw funds from the wallet</mark>) so maybe only send what you will spend at some point.

there are only select stores where this works so check that too.

At the register, have to ask them to run it as a gift card because the cashiers don’t know they can accept bitcoin yet.

<mark class="highlight-orange"><strong>With a little planning you can decide which crypto to use that day based on the market value</strong></mark>. The Gemini dollar (GUSD) which is 1:1 to the US dollar is a stable coin so thats an option if coins are down.</blockquote><p id="d0eb67ff-7b38-415f-8982-4e1c5f9e21d1" class="">It’s worth discussing the final point in the extract from this review that refers to the Gemini dollar (GUSD). This is a USD pegged stable coin backed 100% by USD meaning that for every 1 GUSD, Gemini holds 1 USD for you so that you will always be able to exchange 1 GUSD for 1 USD. The GUSD is useful because it is digital and it <strong><mark class="highlight-orange">allows you to spend your dollars on the blockchain without worrying about price volatility</mark></strong>. This is important because it allows you to take advantage of the fee reduction associated with paying through a decentralised network (vs the financial banking system) whilst not taking the risk that your <a href="https://nypost.com/2021/05/24/bitcoin-pizza-guy-who-squandered-365m-has-no-regrets/">BitCoin become less valuable</a> between buying them and using them to pay for coffee (<a href="https://nypost.com/2021/05/24/bitcoin-pizza-guy-who-squandered-365m-has-no-regrets/">or pizza 🍕</a>).</p>


<div class="responsive-iframe-container">
<iframe class="responsive-iframe" style="border:none" src="https://whimsical.com/embed/Ra2MhTU1TJJwnQ4iKCe6WX@2Ux7TurymN5R9G8W8UHC"></iframe>
</div>
<br>

<p id="b7be8ec9-1ae5-4929-aedc-2f84b3baa0cc" class="">So the final part to review is the cost associated with deposits and withdrawals; how much does it cost to buy the bitcoin for my wallet initially, or how much does it cost to sell my bitcoin so that I can remove the USD and put them in another account/wallet/safe? The following section illustrates these costs with Gemini (taken from the Gemini website).</p><h2 id="426e1a53-aad3-41a2-8fcb-8a9de8648f4e" class="">Deposit / Withdrawal <strong>Fee Examples from</strong><mark class="highlight-blue"><strong> </strong></mark><mark class="highlight-blue"><a href="https://www.gemini.com/fees/mobile-fee-schedule#section-fee-examples"><strong>Gemini</strong></a></mark></h2><blockquote id="d1199cbd-1c72-4141-b7f7-c15b882c86cd" class=""><em><strong>Mobile Order </strong></em><em><mark class="highlight-red"><strong>Buy</strong></mark></em><em><strong> </strong></em><em><mark class="highlight-orange"><strong>BTC for USD</strong></mark></em><em><strong> Example –</strong></em><em> Alice wants to buy $100 of BTC with USD. The prevailing Gemini market price of BTC is $4000 USD. On her mobile application, Alice is provided </em><em><mark class="highlight-orange"><strong>a Quoted Price of $4020 USD to buy 1 BTC</strong></mark></em><em>. This represents the Gemini </em><em><strong><mark class="highlight-orange">market price of $4000 USD</mark></strong></em><em>, plus the </em><em><strong><mark class="highlight-orange">0.50% Convenience Fee</mark></strong></em><em> (Gemini market price × 1.005). When Alice enters her buy Mobile Order for $100 USD, the </em><em><strong><mark class="highlight-orange">Transaction Fee of $2.99</mark></strong></em><em> USD is displayed on her mobile application along with the total BTC amount of 0.02413184 (($100 USD -$2.99 USD)/$4020 USD = 0.02413184 BTC) that she will receive for her buy Mobile Order. Alice swipes up on her mobile application to place her Mobile Order to buy 0.02413184 BTC for $100 USD. Fees are only incurred when her Mobile Order is executed.</em></blockquote><blockquote id="05149ecd-5d47-4ac7-a2db-c788ed67643d" class=""><em><strong>Mobile Order </strong></em><em><mark class="highlight-red"><strong>Sell</strong></mark></em><em><mark class="highlight-orange"><strong> BTC for USD </strong></mark></em><em><strong>Example –</strong></em><em> Arthik wants to sell 0.03 BTC for USD. On his mobile application, Arthik is provided a Quoted Price of $3980 USD to sell 1 BTC. This represents the prevailing Gemini market price of $4000 USD, minus the 0.50% Convenience Fee (Gemini market price × 0.995). When Bob enters his sell Mobile Order for 0.03 BTC, the Transaction Fee of $2.99 USD is displayed on his mobile application along with the total proceeds amount of $116.41 USD ((0.03 * $3980) – $2.99 USD = $116.41 USD) that he will receive for his sell Mobile Order. Arthik swipes up on his mobile application to place his Mobile Order to sell 0.03 BTC and receives $116.41 USD. Fees are only incurred when his Mobile Order is executed.</em></blockquote>

<h1 id="940037ab-b27a-4111-9d4c-4d95e024eb30" class="">Closing thoughts</h1><p id="b8133eee-8687-4398-bb37-fc2d0feed6e1" class="">Adoption of the payments network, Flexa, analysed in this article results in the following key benefits to end users of payments ecosystems:</p><ol type="1" id="7bc0ffd4-3e20-420c-81e3-c1ee09156341" class="numbered-list" start="1"><li>A significant cost saving as a result of not requiring the extensive interchange network currently operated by our financial system.</li></ol><ol type="1" id="c94c6469-43d3-4f0f-88d5-138e99fa7b69" class="numbered-list" start="2"><li>A reduction in some of the security risks associated with payments infrastructure due to decentralised design patterns and requirements of the Flexa network and AMP contract.</li></ol><ol type="1" id="bb2dd1ca-6713-48c4-8387-e6deaf356098" class="numbered-list" start="3"><li>A wider range of exchangeable assets to choose from when purchasing goods for consumers or when receiving payments for goods for merchants.</li></ol><p id="640ee147-d4bc-48b1-aca5-75e0a95de22b" class="">
</p>

</div>
</article>
</body>
</html>