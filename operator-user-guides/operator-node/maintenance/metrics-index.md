This document provides details of metrics collected, including their types, descriptions, and labels.

## Table of Contents

* [otel_scope_info](metrics-index.md#otel_scope_info)
* [ssv_cl_request_duration_seconds_bucket](metrics-index.md#ssv_cl_request_duration_seconds_bucket)
* [ssv_cl_request_duration_seconds_count](metrics-index.md#ssv_cl_request_duration_seconds_count)
* [ssv_cl_request_duration_seconds_sum](metrics-index.md#ssv_cl_request_duration_seconds_sum)
* [ssv_cl_sync_distance](metrics-index.md#ssv_cl_sync_distance)
* [ssv_cl_sync_status](metrics-index.md#ssv_cl_sync_status)
* [ssv_duty_scheduler_executions_total](metrics-index.md#ssv_duty_scheduler_executions_total)
* [ssv_duty_scheduler_slot_ticker_delay_duration_seconds_bucket](metrics-index.md#ssv_duty_scheduler_slot_ticker_delay_duration_seconds_bucket)
* [ssv_duty_scheduler_slot_ticker_delay_duration_seconds_count](metrics-index.md#ssv_duty_scheduler_slot_ticker_delay_duration_seconds_count)
* [ssv_duty_scheduler_slot_ticker_delay_duration_seconds_sum](metrics-index.md#ssv_duty_scheduler_slot_ticker_delay_duration_seconds_sum)
* [ssv_el_request_duration_seconds_bucket](metrics-index.md#ssv_el_request_duration_seconds_bucket)
* [ssv_el_request_duration_seconds_count](metrics-index.md#ssv_el_request_duration_seconds_count)
* [ssv_el_request_duration_seconds_sum](metrics-index.md#ssv_el_request_duration_seconds_sum)
* [ssv_el_sync_distance](metrics-index.md#ssv_el_sync_distance)
* [ssv_el_sync_last_processed_block](metrics-index.md#ssv_el_sync_last_processed_block)
* [ssv_el_sync_status](metrics-index.md#ssv_el_sync_status)
* [ssv_event_syncer_handler_last_processed_block](metrics-index.md#ssv_event_syncer_handler_last_processed_block)
* [ssv_p2p_connections_active](metrics-index.md#ssv_p2p_connections_active)
* [ssv_p2p_connections_connected_total](metrics-index.md#ssv_p2p_connections_connected_total)
* [ssv_p2p_connections_disconnected_total](metrics-index.md#ssv_p2p_connections_disconnected_total)
* [ssv_p2p_discovery_peers_accepted_total](metrics-index.md#ssv_p2p_discovery_peers_accepted_total)
* [ssv_p2p_discovery_peers_rejected_total](metrics-index.md#ssv_p2p_discovery_peers_rejected_total)
* [ssv_p2p_discovery_peers_total](metrics-index.md#ssv_p2p_discovery_peers_total)
* [ssv_p2p_message_validations_accepted_total](metrics-index.md#ssv_p2p_message_validations_accepted_total)
* [ssv_p2p_message_validations_duration_seconds_bucket](metrics-index.md#ssv_p2p_message_validations_duration_seconds_bucket)
* [ssv_p2p_message_validations_duration_seconds_count](metrics-index.md#ssv_p2p_message_validations_duration_seconds_count)
* [ssv_p2p_message_validations_duration_seconds_sum](metrics-index.md#ssv_p2p_message_validations_duration_seconds_sum)
* [ssv_p2p_message_validations_total](metrics-index.md#ssv_p2p_message_validations_total)
* [ssv_p2p_messages_in_total](metrics-index.md#ssv_p2p_messages_in_total)
* [ssv_p2p_messages_out_total](metrics-index.md#ssv_p2p_messages_out_total)
* [ssv_p2p_peers_connected](metrics-index.md#ssv_p2p_peers_connected)
* [ssv_p2p_peers_per_topic](metrics-index.md#ssv_p2p_peers_per_topic)
* [ssv_p2p_peers_per_version](metrics-index.md#ssv_p2p_peers_per_version)
* [ssv_p2p_stream_requests_received_total](metrics-index.md#ssv_p2p_stream_requests_received_total)
* [ssv_p2p_stream_requests_sent_total](metrics-index.md#ssv_p2p_stream_requests_sent_total)
* [ssv_p2p_stream_responses_received_total](metrics-index.md#ssv_p2p_stream_responses_received_total)
* [ssv_p2p_stream_responses_sent_total](metrics-index.md#ssv_p2p_stream_responses_sent_total)
* [ssv_validator_consensus_duration_seconds_bucket](metrics-index.md#ssv_validator_consensus_duration_seconds_bucket)
* [ssv_validator_consensus_duration_seconds_count](metrics-index.md#ssv_validator_consensus_duration_seconds_count)
* [ssv_validator_consensus_duration_seconds_sum](metrics-index.md#ssv_validator_consensus_duration_seconds_sum)
* [ssv_validator_duty_duration_seconds_bucket](metrics-index.md#ssv_validator_duty_duration_seconds_bucket)
* [ssv_validator_duty_duration_seconds_count](metrics-index.md#ssv_validator_duty_duration_seconds_count)
* [ssv_validator_duty_duration_seconds_sum](metrics-index.md#ssv_validator_duty_duration_seconds_sum)
* [ssv_validator_post_consensus_duration_seconds_bucket](metrics-index.md#ssv_validator_post_consensus_duration_seconds_bucket)
* [ssv_validator_post_consensus_duration_seconds_count](metrics-index.md#ssv_validator_post_consensus_duration_seconds_count)
* [ssv_validator_post_consensus_duration_seconds_sum](metrics-index.md#ssv_validator_post_consensus_duration_seconds_sum)
* [ssv_validator_pre_consensus_duration_seconds_bucket](metrics-index.md#ssv_validator_pre_consensus_duration_seconds_bucket)
* [ssv_validator_pre_consensus_duration_seconds_count](metrics-index.md#ssv_validator_pre_consensus_duration_seconds_count)
* [ssv_validator_pre_consensus_duration_seconds_sum](metrics-index.md#ssv_validator_pre_consensus_duration_seconds_sum)
* [ssv_validator_stage_duration_seconds_bucket](metrics-index.md#ssv_validator_stage_duration_seconds_bucket)
* [ssv_validator_stage_duration_seconds_count](metrics-index.md#ssv_validator_stage_duration_seconds_count)
* [ssv_validator_stage_duration_seconds_sum](metrics-index.md#ssv_validator_stage_duration_seconds_sum)
* [ssv_validator_submissions](metrics-index.md#ssv_validator_submissions)
* [ssv_validator_validators_per_status](metrics-index.md#ssv_validator_validators_per_status)

---

### `otel_scope_info`
**Type:** gauge

**Description:** Instrumentation Scope metadata

**Labels:**

- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_cl_request_duration_seconds_bucket`
**Type:** histogram

**Description:** consensus client request duration in seconds

**Labels:**

- `http_request_method`
- `http_route_name`
- `le`
- `otel_scope_name`
- `otel_scope_version`
- `server_address`

---
### `ssv_cl_request_duration_seconds_count`
**Type:** histogram

**Description:** consensus client request duration in seconds

**Labels:**

- `http_request_method`
- `http_route_name`
- `otel_scope_name`
- `otel_scope_version`
- `server_address`

---
### `ssv_cl_request_duration_seconds_sum`
**Type:** histogram

**Description:** consensus client request duration in seconds

**Labels:**

- `http_request_method`
- `http_route_name`
- `otel_scope_name`
- `otel_scope_version`
- `server_address`

---
### `ssv_cl_sync_distance`
**Type:** gauge

**Description:** consensus client syncing distance which is a delta between highest and current blocks

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `server_address`

---
### `ssv_cl_sync_status`
**Type:** gauge

**Description:** beacon node status

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `server_address`
- `ssv_cl_sync_status`

---
### `ssv_duty_scheduler_executions_total`
**Type:** counter

**Description:** total number of duties executed by scheduler

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_beacon_role`

---
### `ssv_duty_scheduler_slot_ticker_delay_duration_seconds_bucket`
**Type:** histogram

**Description:** delay of the slot ticker in seconds

**Labels:**

- `le`
- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_duty_scheduler_slot_ticker_delay_duration_seconds_count`
**Type:** histogram

**Description:** delay of the slot ticker in seconds

**Labels:**

- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_duty_scheduler_slot_ticker_delay_duration_seconds_sum`
**Type:** histogram

**Description:** delay of the slot ticker in seconds

**Labels:**

- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_el_request_duration_seconds_bucket`
**Type:** histogram

**Description:** execution client request duration in seconds

**Labels:**

- `le`
- `otel_scope_name`
- `otel_scope_version`
- `server_address`

---
### `ssv_el_request_duration_seconds_count`
**Type:** histogram

**Description:** execution client request duration in seconds

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `server_address`

---
### `ssv_el_request_duration_seconds_sum`
**Type:** histogram

**Description:** execution client request duration in seconds

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `server_address`

---
### `ssv_el_sync_distance`
**Type:** gauge

**Description:** execution client sync distance which is a delta between highest and current blocks

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `server_address`

---
### `ssv_el_sync_last_processed_block`
**Type:** gauge

**Description:** last processed block by execution client

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `server_address`

---
### `ssv_el_sync_status`
**Type:** gauge

**Description:** execution client sync status

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `server_address`
- `ssv_el_status`

---
### `ssv_event_syncer_handler_last_processed_block`
**Type:** gauge

**Description:** last processed block by event handler

**Labels:**

- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_p2p_connections_active`
**Type:** gauge

**Description:** number of active connections

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_p2p_connection_direction`

---
### `ssv_p2p_connections_connected_total`
**Type:** counter

**Description:** total number of connected peers

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_p2p_connection_direction`

---
### `ssv_p2p_connections_disconnected_total`
**Type:** counter

**Description:** total number of disconnected peers

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_p2p_connection_direction`

---
### `ssv_p2p_discovery_peers_accepted_total`
**Type:** counter

**Description:** total number of peers accepted during discovery

**Labels:**

- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_p2p_discovery_peers_rejected_total`
**Type:** counter

**Description:** total number of peers rejected during discovery

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_p2p_discovery_rejection_reason`

---
### `ssv_p2p_discovery_peers_total`
**Type:** counter

**Description:** total number of peers discovered

**Labels:**

- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_p2p_message_validations_accepted_total`
**Type:** counter

**Description:** total number of messages successfully validated and accepted

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`

---
### `ssv_p2p_message_validations_duration_seconds_bucket`
**Type:** histogram

**Description:** message validation duration

**Labels:**

- `le`
- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_p2p_message_validations_duration_seconds_count`
**Type:** histogram

**Description:** message validation duration

**Labels:**

- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_p2p_message_validations_duration_seconds_sum`
**Type:** histogram

**Description:** message validation duration

**Labels:**

- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_p2p_message_validations_total`
**Type:** counter

**Description:** total number of messages validated

**Labels:**

- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_p2p_messages_in_total`
**Type:** counter

**Description:** total number of inbound messages

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_p2p_message_type`

---
### `ssv_p2p_messages_out_total`
**Type:** counter

**Description:** total number of outbound(broadcasted) messages

**Labels:**

- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_p2p_peers_connected`
**Type:** gauge

**Description:** number of connected peers

**Labels:**

- `otel_scope_name`
- `otel_scope_version`

---
### `ssv_p2p_peers_per_topic`
**Type:** gauge

**Description:** number of connected peers per topic

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_p2p_topic_name`

---
### `ssv_p2p_peers_per_version`
**Type:** gauge

**Description:** number of connected peers per node version

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_node_version`

---
### `ssv_p2p_stream_requests_received_total`
**Type:** counter

**Description:** total number of stream requests received

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_p2p_protocol_id`

---
### `ssv_p2p_stream_requests_sent_total`
**Type:** counter

**Description:** total number of stream requests sent

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_p2p_protocol_id`

---
### `ssv_p2p_stream_responses_received_total`
**Type:** counter

**Description:** total number of stream responses received(as response to initiated by us request)

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_p2p_protocol_id`

---
### `ssv_p2p_stream_responses_sent_total`
**Type:** counter

**Description:** total number of stream responses sent(as response to a peer request)

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_p2p_protocol_id`

---
### `ssv_validator_consensus_duration_seconds_bucket`
**Type:** histogram

**Description:** consensus duration

**Labels:**

- `le`
- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`

---
### `ssv_validator_consensus_duration_seconds_count`
**Type:** histogram

**Description:** consensus duration

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`

---
### `ssv_validator_consensus_duration_seconds_sum`
**Type:** histogram

**Description:** consensus duration

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`

---
### `ssv_validator_duty_duration_seconds_bucket`
**Type:** histogram

**Description:** duty duration

**Labels:**

- `le`
- `otel_scope_name`
- `otel_scope_version`
- `ssv_beacon_role`
- `ssv_validator_duty_round`

---
### `ssv_validator_duty_duration_seconds_count`
**Type:** histogram

**Description:** duty duration

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_beacon_role`
- `ssv_validator_duty_round`

---
### `ssv_validator_duty_duration_seconds_sum`
**Type:** histogram

**Description:** duty duration

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_beacon_role`
- `ssv_validator_duty_round`

---
### `ssv_validator_post_consensus_duration_seconds_bucket`
**Type:** histogram

**Description:** post consensus duration

**Labels:**

- `le`
- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`

---
### `ssv_validator_post_consensus_duration_seconds_count`
**Type:** histogram

**Description:** post consensus duration

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`

---
### `ssv_validator_post_consensus_duration_seconds_sum`
**Type:** histogram

**Description:** post consensus duration

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`

---
### `ssv_validator_pre_consensus_duration_seconds_bucket`
**Type:** histogram

**Description:** pre consensus duration

**Labels:**

- `le`
- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`

---
### `ssv_validator_pre_consensus_duration_seconds_count`
**Type:** histogram

**Description:** pre consensus duration

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`

---
### `ssv_validator_pre_consensus_duration_seconds_sum`
**Type:** histogram

**Description:** pre consensus duration

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`

---
### `ssv_validator_stage_duration_seconds_bucket`
**Type:** histogram

**Description:** validator stage(proposal, prepare, commit) duration

**Labels:**

- `le`
- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`
- `ssv_validator_duty_round`
- `ssv_validator_stage`

---
### `ssv_validator_stage_duration_seconds_count`
**Type:** histogram

**Description:** validator stage(proposal, prepare, commit) duration

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`
- `ssv_validator_duty_round`
- `ssv_validator_stage`

---
### `ssv_validator_stage_duration_seconds_sum`
**Type:** histogram

**Description:** validator stage(proposal, prepare, commit) duration

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_runner_role`
- `ssv_validator_duty_round`
- `ssv_validator_stage`

---
### `ssv_validator_submissions`
**Type:** gauge

**Description:** number of duty submissions

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_beacon_role`

---
### `ssv_validator_validators_per_status`
**Type:** gauge

**Description:** total number of validators by status

**Labels:**

- `otel_scope_name`
- `otel_scope_version`
- `ssv_validator_status`

---
