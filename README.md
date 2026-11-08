# LoRa_Node
Information and immplementaton of a LoRa Node



## Licence
Modern firmware development is rarely built from scratch. When you build a binary for the nRF52840 using Nordic's modern nRF Connect SDK (NCS), the final executable is a static compilation of three distinct software layers:

1. Your Custom Application Code (Your intellectual property).
2. Zephyr RTOS (The underlying open-source operating system).
3. Nordic Proprietary Stacks (Closed-source binaries in nrfxlib governing Bluetooth Low Energy, mesh networking, or hardware cryptography).

Because everything is statically linked into a single .hex or .bin file, choosing a license with a strong Copyleft (like GPLv2 or GPLv3) creates an immediate, unresolvable legal conflict. The GPL demands that everything in the compilation must be opened up under the GPL. Since you do not own Nordic's closed-source Bluetooth blobs, you cannot legally change their license. Therefore, distributing a GPL-licensed firmware binary for a Nordic chip is a direct copyright violation.

The MPL 2.0 resolves this exact dilemma through its innovative file-level Copyleft mechanism.

- Compatibility with Zephyr RTOS (Apache 2.0): Zephyr utilizes the highly permissive Apache 2.0 license. The MPL 2.0 explicitly permits mixing its code with Apache-licensed code within a larger software compilation. They coexist in the final firmware binary without friction.
- Compatibility with Nordic's Proprietary Blobs: The MPL 2.0 states that its copyleft obligations only apply to the specific files originally licensed under the MPL, or direct modifications to those files. It does not extend its open-source requirements to other separately authored files or libraries that are merely linked alongside it. Therefore, Nordic’s closed-source nrfxlib components remain legally protected under the Nordic 5-Clause License, preventing any license breaches.
- It requires source-code availability for modified files upon distribution, but it does not enforce strict structural re-linking mechanics on the final executable form. This makes it far less intimidating for corporate compliance teams while ensuring your individual files stay open.
- It protects your code: If a company modifies your original files, they are legally obligated to publish those specific modifications under the MPL 2.0. The community wins because bugs fixed by commercial entities flow back into the open-source domain.
- It respects commercial boundaries: The company can still keep their proprietary application logic, custom sensors, or secret algorithms in separate, new files completely closed-source.




