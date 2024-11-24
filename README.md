// combat.cs: Handling combat mechanics, attack combos, and power usage

public class CombatSystem : MonoBehaviour {
    public int health;
    public int energy;
    public float attackSpeed;
    private float comboTimer;
    public string[] comboKeys;

    void Update() {
        if (Input.GetKeyDown(KeyCode.Space)) {
            Attack();
        }
    }

    void Attack() {
        if (comboTimer <= 0) {
            // Start new combo attack
            comboTimer = attackSpeed;
            // Execute attack logic
        }
    }

    public void UsePower(string power) {
        if (energy >= 10) {
            // Use power (e.g., elemental attack or blood bending)
            energy -= 10;
        }
    }
}

