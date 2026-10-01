<!--
SPDX-FileCopyrightText: Copyright (c) 2026 NVIDIA CORPORATION & AFFILIATES. All rights reserved.
SPDX-License-Identifier: Apache-2.0
-->

# Astra Polling PoC Test

This document creates a harmless pull request for validating the Astra
governance bot's outbound GitHub polling flow.

Expected behavior:

1. The Astra service detects this open pull request through the GitHub API.
2. The GitHub App posts one proof-of-concept comment.
3. Later polling cycles do not create duplicate comments.
