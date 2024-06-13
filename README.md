JAVA"""
public class Main {
  static String encrypt(String input) {
    StringBuilder encrypted = new StringBuilder();
    for (char c : input.toCharArray()) {
      if (Character.isLetter(c)) {
        if (c == 'z') {
          encrypted.append('a');
        } else if (c == 'Z') {
          encrypted.append('A');
        } else {
          encrypted.append((char) (c + 1));
        }
      } else {
        encrypted.append(c);
      }
    }
    return encrypted.toString();
  }

  static String decrypt(String input) {
    StringBuilder decrypted = new StringBuilder();
    for (char c : input.toCharArray()) {
      if (Character.isLetter(c)) {
        if (c == 'a') {
          decrypted.append('z');
        } else if (c == 'A') {
          decrypted.append('Z');
        } else {
          decrypted.append((char) (c - 1));
        }
      } else {
        decrypted.append(c);
      }
    }
    return decrypted.toString();
  }

  static String needToContactMe() {
    String[] contact = new String[] {"nbjm : wpmfvsefhpvuf@hnbjm.dpn", "qipof : 3630"};

    StringBuilder result = new StringBuilder();
    for (int i = 0; i < contact.length; i++) {
      result.append(contact[i]);
      if (i < contact.length - 1) {
        result.append(", ");
      }
    }
    return result.toString();
  }

  public static void main(String[] args) {
    String encrypted = needToContactMe();
    System.out.println("Need to contact me ? : " + decrypt(encrypted));
  }
}

//have fun  :3
"""
