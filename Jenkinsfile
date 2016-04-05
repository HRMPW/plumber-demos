plumber([
        env: ["ANIMAL": "chicken"],
        
        phases: [
            [
                name: "first-phase",
                action: [
                    name: "inlineDemo",
                    goals: "eat hot dogs"
                ]
            ]
        ],
        debug: true
])

import io.jenkins.plugins.pipelineaction.PipelineAction
import io.jenkins.plugins.pipelineaction.actions.AbstractPipelineActionScript
import org.jenkinsci.plugins.workflow.cps.CpsScript

class inlineDemo extends AbstractPipelineActionScript {
    public inlineDemo(CpsScript script, PipelineAction actionDefinition) {
        super(script, actionDefinition)
    }
    
    def call(Map args) {
            script.sh "echo ${args.goals}"
    }

}
