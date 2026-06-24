# Runtime-cpp2il-dumper
got tired of keys and not being able to access cpp2il externally and stuff so here’s runtime for android


only arm64



got tired of encryption keys requiring me to play the game anyways 
(and was really fun learning how to reverse games like this ) 


forked from samboy just made for android now and dumps at runtime :D


thank samboy for this


dump located
within your sdcard


how to load the libary


**const-string v0, "a365mobproject"

invoke-static {v0}, Ljava/lang/System;->loadLibrary(Ljava/lang/String;)V**



lets say theres some shitty health and death code we will take alot of guesses but mostly accurate

public void TakeDamage(int amount)
{
    health = health - amount;
    if (health <= 0 && !isDead)
    {
        isDead = true;
        Die(); // libil2cpp.so+0x4A21C0
    }
}

this is what my Cpp2il returns 



# issues
doesnt bypass any encryptyion
sometimes foreach for and certain things can be off
can cause extreme loading times and crashing (just remove the lib after its dump :D )
