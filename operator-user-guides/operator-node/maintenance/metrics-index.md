# Metrics Index

This document provides details of metrics collected, including their types, descriptions, and labels.

### Table of Contents

* otel\_scope\_info
* ssv\_cl\_request\_duration\_seconds\_bucket
* ssv\_cl\_request\_duration\_seconds\_count
* ssv\_cl\_request\_duration\_seconds\_sum
* ssv\_cl\_sync\_distance
* ssv\_cl\_sync\_status
* ssv\_duty\_scheduler\_executions\_total
* ssv\_duty\_scheduler\_slot\_ticker\_delay\_duration\_seconds\_bucket
* ssv\_duty\_scheduler\_slot\_ticker\_delay\_duration\_seconds\_count
* ssv\_duty\_scheduler\_slot\_ticker\_delay\_duration\_seconds\_sum
* ssv\_el\_request\_duration\_seconds\_bucket
* ssv\_el\_request\_duration\_seconds\_count
* ssv\_el\_request\_duration\_seconds\_sum
* ssv\_el\_sync\_distance
* ssv\_el\_sync\_last\_processed\_block
* ssv\_el\_sync\_status
* ssv\_event\_syncer\_handler\_last\_processed\_block
* ssv\_p2p\_connections\_active
* ssv\_p2p\_connections\_connected\_total
* ssv\_p2p\_connections\_disconnected\_total
* ssv\_p2p\_discovery\_peers\_accepted\_total
* ssv\_p2p\_discovery\_peers\_rejected\_total
* ssv\_p2p\_discovery\_peers\_total
* ssv\_p2p\_message\_validations\_accepted\_total
* ssv\_p2p\_message\_validations\_duration\_seconds\_bucket
* ssv\_p2p\_message\_validations\_duration\_seconds\_count
* ssv\_p2p\_message\_validations\_duration\_seconds\_sum
* ssv\_p2p\_message\_validations\_total
* ssv\_p2p\_messages\_in\_total
* ssv\_p2p\_messages\_out\_total
* ssv\_p2p\_peers\_connected
* ssv\_p2p\_peers\_per\_topic
* ssv\_p2p\_peers\_per\_version
* ssv\_p2p\_stream\_requests\_received\_total
* ssv\_p2p\_stream\_requests\_sent\_total
* ssv\_p2p\_stream\_responses\_received\_total
* ssv\_p2p\_stream\_responses\_sent\_total
* ssv\_validator\_consensus\_duration\_seconds\_bucket
* ssv\_validator\_consensus\_duration\_seconds\_count
* ssv\_validator\_consensus\_duration\_seconds\_sum
* ssv\_validator\_duty\_duration\_seconds\_bucket
* ssv\_validator\_duty\_duration\_seconds\_count
* ssv\_validator\_duty\_duration\_seconds\_sum
* ssv\_validator\_post\_consensus\_duration\_seconds\_bucket
* ssv\_validator\_post\_consensus\_duration\_seconds\_count
* ssv\_validator\_post\_consensus\_duration\_seconds\_sum
* ssv\_validator\_pre\_consensus\_duration\_seconds\_bucket
* ssv\_validator\_pre\_consensus\_duration\_seconds\_count
* ssv\_validator\_pre\_consensus\_duration\_seconds\_sum
* ssv\_validator\_stage\_duration\_seconds\_bucket
* ssv\_validator\_stage\_duration\_seconds\_count
* ssv\_validator\_stage\_duration\_seconds\_sum
* ssv\_validator\_submissions
* ssv\_validator\_validators\_per\_status

***

#### `otel_scope_info`

**Type:** gauge

**Description:** Instrumentation Scope metadata

**Labels:**

* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_cl_request_duration_seconds_bucket`

**Type:** histogram

**Description:** consensus client request duration in seconds

**Labels:**

* `http_request_method`
* `http_route_name`
* `le`
* `otel_scope_name`
* `otel_scope_version`
* `server_address`

***

#### `ssv_cl_request_duration_seconds_count`

**Type:** histogram

**Description:** consensus client request duration in seconds

**Labels:**

* `http_request_method`
* `http_route_name`
* `otel_scope_name`
* `otel_scope_version`
* `server_address`

***

#### `ssv_cl_request_duration_seconds_sum`

**Type:** histogram

**Description:** consensus client request duration in seconds

**Labels:**

* `http_request_method`
* `http_route_name`
* `otel_scope_name`
* `otel_scope_version`
* `server_address`

***

#### `ssv_cl_sync_distance`

**Type:** gauge

**Description:** consensus client syncing distance which is a delta between highest and current blocks

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `server_address`

***

#### `ssv_cl_sync_status`

**Type:** gauge

**Description:** beacon node status

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `server_address`
* `ssv_cl_sync_status`

***

#### `ssv_duty_scheduler_executions_total`

**Type:** counter

**Description:** total number of duties executed by scheduler

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_beacon_role`

***

#### `ssv_duty_scheduler_slot_ticker_delay_duration_seconds_bucket`

**Type:** histogram

**Description:** delay of the slot ticker in seconds

**Labels:**

* `le`
* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_duty_scheduler_slot_ticker_delay_duration_seconds_count`

**Type:** histogram

**Description:** delay of the slot ticker in seconds

**Labels:**

* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_duty_scheduler_slot_ticker_delay_duration_seconds_sum`

**Type:** histogram

**Description:** delay of the slot ticker in seconds

**Labels:**

* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_el_request_duration_seconds_bucket`

**Type:** histogram

**Description:** execution client request duration in seconds

**Labels:**

* `le`
* `otel_scope_name`
* `otel_scope_version`
* `server_address`

***

#### `ssv_el_request_duration_seconds_count`

**Type:** histogram

**Description:** execution client request duration in seconds

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `server_address`

***

#### `ssv_el_request_duration_seconds_sum`

**Type:** histogram

**Description:** execution client request duration in seconds

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `server_address`

***

#### `ssv_el_sync_distance`

**Type:** gauge

**Description:** execution client sync distance which is a delta between highest and current blocks

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `server_address`

***

#### `ssv_el_sync_last_processed_block`

**Type:** gauge

**Description:** last processed block by execution client

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `server_address`

***

#### `ssv_el_sync_status`

**Type:** gauge

**Description:** execution client sync status

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `server_address`
* `ssv_el_status`

***

#### `ssv_event_syncer_handler_last_processed_block`

**Type:** gauge

**Description:** last processed block by event handler

**Labels:**

* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_p2p_connections_active`

**Type:** gauge

**Description:** number of active connections

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_p2p_connection_direction`

***

#### `ssv_p2p_connections_connected_total`

**Type:** counter

**Description:** total number of connected peers

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_p2p_connection_direction`

***

#### `ssv_p2p_connections_disconnected_total`

**Type:** counter

**Description:** total number of disconnected peers

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_p2p_connection_direction`

***

#### `ssv_p2p_discovery_peers_accepted_total`

**Type:** counter

**Description:** total number of peers accepted during discovery

**Labels:**

* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_p2p_discovery_peers_rejected_total`

**Type:** counter

**Description:** total number of peers rejected during discovery

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_p2p_discovery_rejection_reason`

***

#### `ssv_p2p_discovery_peers_total`

**Type:** counter

**Description:** total number of peers discovered

**Labels:**

* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_p2p_message_validations_accepted_total`

**Type:** counter

**Description:** total number of messages successfully validated and accepted

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`

***

#### `ssv_p2p_message_validations_duration_seconds_bucket`

**Type:** histogram

**Description:** message validation duration

**Labels:**

* `le`
* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_p2p_message_validations_duration_seconds_count`

**Type:** histogram

**Description:** message validation duration

**Labels:**

* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_p2p_message_validations_duration_seconds_sum`

**Type:** histogram

**Description:** message validation duration

**Labels:**

* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_p2p_message_validations_total`

**Type:** counter

**Description:** total number of messages validated

**Labels:**

* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_p2p_messages_in_total`

**Type:** counter

**Description:** total number of inbound messages

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_p2p_message_type`

***

#### `ssv_p2p_messages_out_total`

**Type:** counter

**Description:** total number of outbound(broadcasted) messages

**Labels:**

* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_p2p_peers_connected`

**Type:** gauge

**Description:** number of connected peers

**Labels:**

* `otel_scope_name`
* `otel_scope_version`

***

#### `ssv_p2p_peers_per_topic`

**Type:** gauge

**Description:** number of connected peers per topic

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_p2p_topic_name`

***

#### `ssv_p2p_peers_per_version`

**Type:** gauge

**Description:** number of connected peers per node version

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_node_version`

***

#### `ssv_p2p_stream_requests_received_total`

**Type:** counter

**Description:** total number of stream requests received

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_p2p_protocol_id`

***

#### `ssv_p2p_stream_requests_sent_total`

**Type:** counter

**Description:** total number of stream requests sent

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_p2p_protocol_id`

***

#### `ssv_p2p_stream_responses_received_total`

**Type:** counter

**Description:** total number of stream responses received(as response to initiated by us request)

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_p2p_protocol_id`

***

#### `ssv_p2p_stream_responses_sent_total`

**Type:** counter

**Description:** total number of stream responses sent(as response to a peer request)

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_p2p_protocol_id`

***

#### `ssv_validator_consensus_duration_seconds_bucket`

**Type:** histogram

**Description:** consensus duration

**Labels:**

* `le`
* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`

***

#### `ssv_validator_consensus_duration_seconds_count`

**Type:** histogram

**Description:** consensus duration

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`

***

#### `ssv_validator_consensus_duration_seconds_sum`

**Type:** histogram

**Description:** consensus duration

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`

***

#### `ssv_validator_duty_duration_seconds_bucket`

**Type:** histogram

**Description:** duty duration

**Labels:**

* `le`
* `otel_scope_name`
* `otel_scope_version`
* `ssv_beacon_role`
* `ssv_validator_duty_round`

***

#### `ssv_validator_duty_duration_seconds_count`

**Type:** histogram

**Description:** duty duration

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_beacon_role`
* `ssv_validator_duty_round`

***

#### `ssv_validator_duty_duration_seconds_sum`

**Type:** histogram

**Description:** duty duration

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_beacon_role`
* `ssv_validator_duty_round`

***

#### `ssv_validator_post_consensus_duration_seconds_bucket`

**Type:** histogram

**Description:** post consensus duration

**Labels:**

* `le`
* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`

***

#### `ssv_validator_post_consensus_duration_seconds_count`

**Type:** histogram

**Description:** post consensus duration

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`

***

#### `ssv_validator_post_consensus_duration_seconds_sum`

**Type:** histogram

**Description:** post consensus duration

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`

***

#### `ssv_validator_pre_consensus_duration_seconds_bucket`

**Type:** histogram

**Description:** pre consensus duration

**Labels:**

* `le`
* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`

***

#### `ssv_validator_pre_consensus_duration_seconds_count`

**Type:** histogram

**Description:** pre consensus duration

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`

***

#### `ssv_validator_pre_consensus_duration_seconds_sum`

**Type:** histogram

**Description:** pre consensus duration

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`

***

#### `ssv_validator_stage_duration_seconds_bucket`

**Type:** histogram

**Description:** validator stage(proposal, prepare, commit) duration

**Labels:**

* `le`
* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`
* `ssv_validator_duty_round`
* `ssv_validator_stage`

***

#### `ssv_validator_stage_duration_seconds_count`

**Type:** histogram

**Description:** validator stage(proposal, prepare, commit) duration

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`
* `ssv_validator_duty_round`
* `ssv_validator_stage`

***

#### `ssv_validator_stage_duration_seconds_sum`

**Type:** histogram

**Description:** validator stage(proposal, prepare, commit) duration

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_runner_role`
* `ssv_validator_duty_round`
* `ssv_validator_stage`

***

#### `ssv_validator_submissions`

**Type:** gauge

**Description:** number of duty submissions

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_beacon_role`

***

#### `ssv_validator_validators_per_status`

**Type:** gauge

**Description:** total number of validators by status

**Labels:**

* `otel_scope_name`
* `otel_scope_version`
* `ssv_validator_status`

***