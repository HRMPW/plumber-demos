plumber([
        env: ["ANIMAL": "chicken"],
        
        phases: [
            [
                name: "first-phase",
                action: [
                    script: 'echo "I am an animal of type ${ANIMAL}"'
                ]
            ],

            [
                name: "split-phases-1",
                env: ["ANIMAL": "cat"],
                action: [
                    script: 'echo "I am an animal of type ${ANIMAL}"'
                ],
                after: "first-phase"
            ],

            [
                name: "split-phases-2",
                env: ["ANIMAL": "dog"],
                action: [
                    script: 'echo "I am an animal of type ${ANIMAL}"'
                ],
                after: "first-phase"
            ],

            [
                name: "joined-phase",
                env: ["ANIMAL": "monkey"],
                action: [
                    script: 'echo "I am an animal of type ${ANIMAL}"'
                ],
                after: ["split-phases-1", "split-phases-2"]
            ]
        ],
        debug: true
])