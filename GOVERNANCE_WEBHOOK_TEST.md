<!--
SPDX-FileCopyrightText: Copyright (c) 2026 NVIDIA CORPORATION & AFFILIATES. All rights reserved.
SPDX-License-Identifier: Apache-2.0
-->

# Governance webhook delivery test

This file provides a small pull-request fixture for testing the Governance PoC
webhook receiver in `lavanyavijayk/dynamo-test`.

Opening this pull request should send a `pull_request` event with action `opened`.
The receiver should verify the signature and repository allowlist, record receipt
metadata, and return HTTP 202. Redelivering the same event should return HTTP 202
with a duplicate acknowledgement.

The current receiver runs in receipt-only mode; it does not analyze code or post
comments. This fixture is intended for the test fork and does not need to merge.
