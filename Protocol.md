Protocol design documentation


full packet structure:                     [0, 11)
[link_hdr][onion_hdr][data..padded to (1024 - sizeof(link_hdr) - sizeof(onion_hdr))][tag0..tag11]..padded to 1200-bytes


link hdr:   offset is 16-bytes because UDP packet can only be 65535 bytes large
[packet_len: usize][offset: u16][sequence_num: u32][data(onion_hdr + payload + tags + padding to 1200)]

onion_hdr:
[]

payload:


relay_payload:


tag stuff:

